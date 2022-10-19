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

** :wrench: Configure your NPM_CENCO_TOKEN**\
Required to install @library/cenco-ux-components

```bash
# Generate your token in Gitlab > Preferences > Access Tokens > scope "read_api"

export NPM_CENCO_TOKEN=<put your token generated here>
```

**Install node dependencies**

```bash
npm install
```

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
