# Hathora Cloud API

Tagging a release on this repository will update the:

- [Node.js SDK repo](https://github.com/fern-hathora/hathora-node)
- _More SDKs to come..._

## What is in this repository?

This repository contains

- Hathora's OpenAPI Definition which lives in the [openapi](./fern/api/openapi/) folder
- Generators (see [generators.yml](./fern/api/generators.yml))

To make sure that the OpenAPI is valid, you can use the Fern CLI.

```bash
npm install -g fern-api # Installs CLI
fern check # Checks if the definition is valid
```

## What are generators?

Generators read in your API Definition and output artifacts (e.g. the TypeScript SDK Generator) and are tracked in [generators.yml](./fern/api/generators.yml).

To trigger the generators run:

```bash
fern generate --group external --version <version>
```

This command currently runs in a GitHub workflow (see [ci.yml](.github/workflows/ci.yml#L32))
