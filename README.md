# mf-app-resume-header

- Microfrontend application of the header of the resume page.

## Getting started

Configure your **NPM_CENCO_TOKEN**
Required to install @library/cenco-ux-components

```bash
# Generate your token in Gitlab > Preferences > Access Tokens > scope "read_api"

export NPM_CENCO_TOKEN=<put your token generated here>
```

Install dependencies

```bash
npm install
```

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

docker-compose run --rm --service-ports mf-app npm run start:standalone
```

Run the microfront in **server mode**:

```bash
# next command start your microfront in http://localhost:8080 to be used in the root-config

docker-compose run --rm --service-ports mf-app
```

Build and Start the microfront in **server mode**:

```bash
# next command start your microfront in http://localhost:8080 to be used in the root-config

docker-compose up
```
