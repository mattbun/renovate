# renovate

A common renovate config for my projects.

## Usage

Put this in `renovate.json`:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>mattbun/renovate"
  ]
}
```

Node.js docker image updates require the Node.js version to be in an `ARG`, like this:

```dockerfile
ARG NODE_VERSION=18.14.2
FROM node:${NODE_VERSION}-alpine AS build
```