# SolidLabLib.js - Lib

[![Build status](https://github.com/SolidLabResearch/SolidLabLib.js/workflows/CI/badge.svg)](https://github.com/SolidLabResearch/SolidLabLib.js/actions?query=workflow%3ACI)
[![Coverage Status](https://coveralls.io/repos/github/SolidLabResearch/SolidLabLib.js/badge.svg?branch=master)](https://coveralls.io/github/SolidLabResearch/SolidLabLib.js?branch=master)
[![npm version](https://badge.fury.io/js/%40solidlab%2Flib.svg)](https://www.npmjs.com/package/@solidlab/lib)

A library of helper functions for developing Solid apps in TypeScript/JavaScript.

This package is a bundle of _all_ helper functions defined in SolidLabLib.
[These functions can also be installed separately](https://github.com/SolidLabResearch/SolidLabLib.js/).

## Requirements

* [Node.js](https://nodejs.org/en/) _(1.14 or higher)_

## Installation

```bash
$ npm install @solidlab/lib
```
or
```bash
$ yarn add @solidlab/lib
```

## Usage

### Obtain the identity provider

_This canonical package of this function is [`@solidlab/idp`](https://github.com/SolidLabResearch/SolidLabLib.js/tree/master/packages/idp)_

The identity provider of a WebID can be determined as follows:
```typescript
import { defaultSolidUtilContext, getIdp } from '@solidlab/lib';

await getIdp('https://rubensworks.solidcommunity.net/profile/card#me', defaultSolidUtilContext());
```

If you have an authenticated Solid session object, you can determine its IDP as follows:
```typescript
await getIdp(session.info.webId, defaultSolidUtilContext(session));
```

## License

This code is copyrighted by [Ghent University – imec](http://idlab.ugent.be/)
and released under the [MIT license](http://opensource.org/licenses/MIT).
