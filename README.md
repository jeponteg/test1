# mf-app-resume-skeleton-easy

This Microfrontend previews your content before the data is loaded to reduce load time frustration.

## Getting started

**Update your Atom name!**\
Open your terminal an run this command to update the name of your Atom in all required files:

```bash
npx replace 'apps-template' '<your-atom-name>' package.json package-lock.json tsconfig.json webpack.config.js
```

Then, rename the entypoint file with the name of your atom

```bash
mv src/cencommerce-apps-template.tsx src/cencommerce-<your-atom-name>.tsx
```

**Configure your NPM_CENCO_TOKEN**\
Required to install @library/cenco-ux-components

```bash
# Generate your token in Gitlab > Preferences > Access Tokens > scope "read_api"

export NPM_CENCO_TOKEN=<put your token generated here>
```

**Install node dependencies**

```bash
npm install
```

## Folders structure

The src folder is structure following [atomic design](https://bradfrost.com/blog/post/atomic-web-design/) pattern:

- Atoms
- Molecules
- Organisms
- Templates
- Pages

So put your components in the proper folder, and the storybook title must keep the same structure e.g.

```js
const meta: Meta = {
  title: 'Atoms/Title',
  component: Title,
};
```

## Run commands

Run microfront **storybook**:

```bash
# next command start storybook in http://localhost:6006

npm run storybook
```

Run microfront in **standalone mode**:

```bash
# next command start your microfront in http://localhost:8080

npm run start:standalone
```

Run microfront in **server mode**:

```bash
# next command start your microfront in http://localhost:8080 to be used in the root-config

npm run start
```

## Running using Docker

Copy your NPM_CENCO_TOKEN in your **.env** file

```bash
# Generate your token in Gitlab > Preferences > Access Tokens > scope "read_api"

NPM_CENCO_TOKEN=<put your token generated here>
```

Build the microfront service:

```bash
docker-compose build
```

Run microfront **storybook**:

```bash
# next command start storybook in http://localhost:6006

docker-compose run --rm -p 6006:6006 mf-app npm run storybook
```

Run microfront in **standalone mode**:

```bash
# next command start your microfront in http://localhost:8080

docker-compose run --rm -p 8080:8080 mf-app npm run start:standalone
```

Run the microfront in **server mode**:

```bash
# next command start your microfront in http://localhost:8080 to be used in the root-config

docker-compose run --rm -p 8080:8080 mf-app
```

Build and Start the microfront in **server mode**:

```bash
# next command start your microfront in http://localhost:8080 to be used in the root-config

docker-compose up
```

## Usage

## Props


| Prop name     | type                        | Description |
| ------------- | --------------------------- | ----------- |
| classes       | string                      | Description |
| Color         | string                      | Description |
| variante      | 'vBar', 'hBar', 'circle'    | Description |
| type          | string                      | Description |
| size          | 'xs','sm','md','lg','full'  | Description |
