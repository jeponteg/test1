# mfe-app-resume-header/app

This Microfrontend displays a view of the header in the my purchases session.

![mfe-app-resume-header/app](https://i.ibb.co/xS368ff/Captura-de-Pantalla-2022-10-04-a-la-s-12-58-02.png)

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
Required to install @mfe-app-resume-header/app

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

## Props


| Prop name     | type                            | Description                                                                                          |
| ------------- | --------------------------------| -----------------------------------------------------------------------------------------------------| 
| classes       | string                          | This prop receives the css classes from the framework tailwindcss                                    |
| color         | string                          | This pro changes the color of the component                                                          | 
| variante      | 'vBar', 'hBar', 'circle'        | Variants are the forms that your component can be adapted to. (circle, horizontal bar, vertical bar) |
| size          | 'xs', 'sm', 'md', 'lg', 'full'  | This prop is used to set the size of the component                                                   |


[To see the effects of the application of these pros, you can click on this link](https://self-service-cenco-ux-components.ecomm-stg.cencosud.com/?path=/story/components-commons-layout-skeleton--horizontal-bar)

## Customization

In order to apply CSS customizations in this aplication, follow the instructions given in the recipe on Using CSS with [tailwindcss](https://tailwindcss.com/)

This css framework is configured in the project to use the "tw-" prefix

```bash
  # example:
  
  <Skeleton classes="tw-h-[22px] tw-w-[99px] tw-mb-2"/>

```
