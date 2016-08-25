## Introduction

[![Join the chat at https://gitter.im/s0ph1e/node-css-url-parser](https://badges.gitter.im/s0ph1e/node-css-url-parser.svg)](https://gitter.im/s0ph1e/node-css-url-parser?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
Parse urls from css file

[![Build Status](https://img.shields.io/travis/s0ph1e/node-css-url-parser/master.svg?style=flat)](https://travis-ci.org/s0ph1e/node-css-url-parser)
[![Coverage Status](https://coveralls.io/repos/s0ph1e/node-css-url-parser/badge.svg)](https://coveralls.io/r/s0ph1e/node-css-url-parser)
[![Code Climate](https://codeclimate.com/github/s0ph1e/node-css-url-parser/badges/gpa.svg)](https://codeclimate.com/github/s0ph1e/node-css-url-parser)
[![Version](https://img.shields.io/npm/v/css-url-parser.svg?style=flat)](https://www.npmjs.org/package/css-url-parser)
[![Downloads](https://img.shields.io/npm/dm/css-url-parser.svg?style=flat)](https://www.npmjs.org/package/css-url-parser)
[![Dependency Status](https://david-dm.org/s0ph1e/node-css-url-parser.svg?style=flat)](https://david-dm.org/s0ph1e/node-css-url-parser)


## Installation
```
npm install css-url-parser
```

## Usage
```javascript
var parseCssUrls = require('css-url-parser');

var css = '@import "a.css"; .image { background-image: url(images/img.png); }';
var cssUrls = parseCssUrls(css);

console.log(cssUrls);   // [ 'a.css', 'images/img.png' ]
```

It ignores duplicated urls and base64 encoded resources.
If no urls found empty array will be returned.
