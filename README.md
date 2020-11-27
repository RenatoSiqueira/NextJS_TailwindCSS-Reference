# Como Integrar NextJS com TailwindCSS

## Instale os pacotes:

(Se já tiver instalado o next, react e react-dom, pode apagar da linha.)

```
npm install next react react-dom tailwindcss postcss autoprefixer
```

## Crie um arquivo postcss.config.js na raiz e adicione:

```javascript
// postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};
```

## Use o gerador do Tailwind:

(Ele criará o tailwind.config.js)

```
npx tailwindcss init
```

## - Crie uma pasta css

## - Dentro dela, crie o styles.css com este conteúdo:

```css
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
```

## Faça a importação no pages/\_app.js

```javascript
import React from "react";
import "../css/styles.css"; // <- Aqui

const MyApp = ({ Component, pageProps }) => <Component {...pageProps} />;

export default MyApp;
```

## Teste!

```
npm run dev
```

### Observações:

Certifique-se de que seu package.json já está com os scripts:

```javascript
  "scripts": {
    "dev": "next",
    "start": "next start",
    "build": "next build"
  },
```
