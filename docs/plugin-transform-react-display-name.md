---
id: babel-plugin-transform-react-display-name
title: "@babel/plugin-transform-react-display-name"
sidebar_label: react-display-name
---

:::info
This plugin is included in `@babel/preset-react`
:::

## Example

**In**

```js title="JavaScript"
var foo = React.createClass({}); // React <= 15
var bar = createReactClass({}); // React 16+
```

**Out**

```js title="JavaScript"
var foo = React.createClass({
  displayName: "foo",
}); // React <= 15
var bar = createReactClass
babel --plugins @babel/plugin-transform-react-display-name script.js
```

### Via Node API

```js title="JavaScript"
require("@babel/core").transformSync("code", {
  plugins: ["@babel/plugin-transform-react-display-name"],
});
```
