Guide: https://tailwindcss.com/docs/guides/create-react-app

## Install Tailwind

`npm install -D tailwindcss@npm:@tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9`

## Install CRACO

`npm install @craco/craco`

Update package.json
```  {
    "scripts": {
     <!-- "start": "react-scripts start", -->
     <!-- "build": "react-scripts build", -->
     <!-- "test": "react-scripts test", -->
     "start": "craco start",
     "build": "craco build",
     "test": "craco test",
      "eject": "react-scripts eject"
    },
  }
```

Add craco.config.js

```
module.exports = {
  style: {
    postcss: {
      plugins: [
        require('tailwindcss'),
        require('autoprefixer'),
      ],
    },
  },
}
```

## Tailwind config file

`npx tailwindcss-cli@latest init`


## Include Tailwind in CSS

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

