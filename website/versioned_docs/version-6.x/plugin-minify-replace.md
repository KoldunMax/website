---
# Don't edit this file directly, it was copied using scripts/download-readmes.js: 
id: version-6.x-babel-plugin-minify-replace
title: babel-plugin-minify-replace
sidebar_label: minify-replace
original_id: babel-plugin-minify-replace
---

## Example

**Options**

```javascript
[
  {
    identifierName: "__DEV__",
    replacement: {
      type: "numericLiteral",
      value: 0,
    },
  },
]
```

**In**

```javascript
if (!__DEV__) {
  foo();
}
if (a.__DEV__) {
  foo();
}
```

**Out**

```javascript
if (!0) {
  foo();
}
if (a.__DEV__) {
  foo();
}
```

## Installation

```sh
npm install babel-plugin-minify-replace
```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
// without options
{
  "plugins": ["minify-replace"]
}
```

```json
// with options
{
  "plugins": [
    ["minify-replace", {
      "replacements": [{
        "identifierName": "__DEV__",
        "replacement": {
          "type": "booleanLiteral",
          "value": true
        }
      }]
    }]
  ]
}
```

### Via CLI

```sh
babel --plugins minify-replace script.js
```

### Via Node API

```javascript
require("babel-core").transform("code", {
  plugins: ["minify-replace"]
});
```

