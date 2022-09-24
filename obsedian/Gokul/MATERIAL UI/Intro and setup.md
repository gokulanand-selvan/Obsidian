***1) What is material UI?***

- Material UI is an open-source React component library that implements Google's [Material Design](https://material.io/).

- It includes a comprehensive collection of prebuilt components that are ready for use in production right out of the box.

- Material UI is beautiful by design and features a suite of customization options that make it easy to implement your own custom design system on top of our components.

***2) Installation***

## npm

- To install and save in your `package.json` dependencies, run the command below using **npm**:

```sh
npm install @mui/material @emotion/react @emotion/styled
```

- Material UI is using [emotion](https://emotion.sh/docs/introduction)  {*Emotion* is a *library* used foe writing CSS with JavaScript}as a styling engine by default. If you want to use [`styled-components`](https://styled-components.com/) instead, run:


```sh
npm install @mui/material @mui/styled-engine-sc styled-components
```

## Roboto font

Material UI was designed with the [Roboto](https://fonts.google.com/specimen/Roboto) font in mind. So be sure to follow [these instructions](https://mui.com/material-ui/react-typography/#general). For instance, via Google Web Fonts:

```html
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700&display=swap"
/>
```

## Font icons

To use the font `Icon` component, you must first add the [Material Icons](https://fonts.google.com/icons?icon.set=Material+Icons) font. Here are [some instructions](https://mui.com/material-ui/icons/#font-icons) on how to do so. For instance, via Google Web Fonts:

```html
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/icon?family=Material+Icons"
/>
```

## SVG icons

In order to use prebuilt SVG Material icons, such as those found in the [icons demos](https://mui.com/material-ui/icons/) you must first install the [@mui/icons-material](https://www.npmjs.com/package/@mui/icons-material) package:

With **npm**:

```sh
npm install @mui/icons-material
```




