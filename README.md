# react-scripts-ts

This package includes scripts and configuration used by [Create React App](https://github.com/facebookincubator/create-react-app).<br>
Please refer to its documentation:

* [Getting Started]

``` bash
$ create-react-app my-ts-app --scripts-version=@baristalabs/react-scripts-ts
```

Additional Resources
---(https://github.com/facebookincubator/create-react-app/blob/master/README.md#getting-started) – How to create a new app.
* [User Guide](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md) – How to develop apps bootstrapped with Create React App.

Enhancements:
---
 - Typescript Support via Awesome-Typescript-Loader & tslint support.
- Additional loaders: scss-loader, worker-loader, raw-loader
- Webpack 4.x support.

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
Incorporates suggestions from https://developer.epages.com/blog/tech-stories/typescript-codesplitting-treeshaking/ for code splitting and tree shaking.