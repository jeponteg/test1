# mf-app-resume-skeleton-easy

This application allows the user to filter their purchases.

![mf-app-resume-searchbox-easy](https://i.ibb.co/hFxd3Vx/Captura-de-Pantalla-2022-10-18-a-la-s-22-11-56.png)

## Folders structure

The src folder is structure following [atomic design](https://bradfrost.com/blog/post/atomic-web-design/) pattern:

- :file_folder: Atoms
- :file_folder: Molecules
- :file_folder: Organisms
- :file_folder: Templates
- :file_folder: Pages


## Getting started

:wrench:  **Configure your NPM_CENCO_TOKEN**\
  Required to install @library/cenco-ux-components

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

