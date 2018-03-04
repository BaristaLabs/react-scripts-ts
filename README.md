# react-scripts-ts

This package forks [create-react-app-typescript](https://github.com/wmonk/create-react-app-typescript) and adds additional loaders, plugins and newer webpack usage as described below.

Getting Started
---

``` bash
$ create-react-app my-ts-app --scripts-version=@baristalabs/react-scripts-ts
```

Additional Resources
--
* [Getting Started](https://github.com/facebookincubator/create-react-app/blob/master/README.md#getting-started) – How to create a new app.
* [User Guide](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md) – How to develop apps bootstrapped with Create React App.

Enhancements over create-react-app-typescript:
---
 - Better Typescript Support via Awesome-Typescript-Loader & tslint support.
   - Note: some of the benefits of awesome-typescript-loader have been superceeded - both babel and fork checking is now in ts-loader, so... will re-evaluate later.
   - fork-ts-checker-webpack-plugin doesn't seem to be picking up configuration and is looking at all files, not just /src/**.*
 - Polyfills via core.js
 - Additional loaders:
   - scss-loader (\*.scss and inline)
   - worker-loader (\*.worker.js and inline)
   - raw-loader (.tsc .tsxc and inline)
 - Webpack 3.x support.
 - Produces runtime/vendor/main files as seperate chunks
 - Incorporates suggestions for [code splitting and tree shaking](https://developer.epages.com/blog/tech-stories/typescript-codesplitting-treeshaking/).

Loader support in Typescript:
---

update tsconfig.json and add loaders via:

```
"compilerOptions" {
    "paths": {
        "loader!*" : ["*"]
    }
}
```

See: https://github.com/Microsoft/TypeScript/issues/10988
