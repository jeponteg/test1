# mfe-app-resume-header/app

This Microfrontend displays a view of the header in the my purchases session.

![mfe-app-resume-header/app](https://i.ibb.co/xS368ff/Captura-de-Pantalla-2022-10-04-a-la-s-12-58-02.png)

## Getting started

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

