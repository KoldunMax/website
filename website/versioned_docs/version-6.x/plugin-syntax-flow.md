---
# Don't edit this file directly, it was copied using scripts/download-readmes.js: 
id: version-6.x-babel-plugin-syntax-flow
title: babel-plugin-syntax-flow
sidebar_label: syntax-flow
original_id: babel-plugin-syntax-flow
---

## Installation

```sh
npm install --save-dev babel-plugin-syntax-flow
```

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
{
  "plugins": ["syntax-flow"]
}
```

### Via CLI

```sh
babel --plugins syntax-flow script.js
```

### Via Node API

```javascript
require("babel-core").transform("code", {
  plugins: ["syntax-flow"]
});
```

