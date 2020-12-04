# Oats Koa Adapter

Oats Koa Adapter is a library that binds server endpoints written with [Oats][1] to [Koa's][2] `Router` object.

## Installation

Use `npm` or `yarn` to install `oats-koa-adapter`.

```bash
npm install oats-koa-adapter
```

## Usage

Oats Koa Adapter exports a single `bind` function. This function is generally used when setting up the router for your application.

### Basic Example

```ts
import * as koaAdapter from '@smartlyio/koa-oats-adapter';
import * as oaserver from '<Your Generated Server>';
import spec from '<Your Route Definitions>';

export const router = () => {
  const requestContextCreator = (ctx: any): any => ctx;

  return koaAdapter.bind(oaserver.router, spec, requestContextCreator);
};
```


[1]: [Oats](https://github.com/smartlyio/oats) is a library that parses OpenAPI specifications and generates client and server code in TypeScript.
[2]: [Koa](https://koajs.com/) is a web framework for node.js applications.
