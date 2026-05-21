# XTrace Memory docs

Public docs for the [`@xtraceai/memory`](https://www.npmjs.com/package/@xtraceai/memory) SDK and the underlying HTTP API. Built with [Mintlify](https://mintlify.com).

## Local development

```bash
npm i -g mintlify
mintlify dev
# → http://localhost:3000
```

## Structure

| File / dir | Purpose |
|---|---|
| `docs.json` | Mintlify config: nav, branding, theme, OpenAPI source |
| `introduction.mdx` | Landing page |
| `guides/` | Hand-written prose guides (quickstart, auth, ingest, search) |
| `api-reference/` | Auto-generated from the OpenAPI spec at `https://api.staging.xtrace.ai/openapi.json` |

## Deploying

Mintlify auto-deploys on push to `main` once the GitHub app is installed on this repo.

## Updating the OpenAPI source

The API Reference is generated from a live URL declared in `docs.json` (`navigation.tabs[].openapi.source`). When the backend ships changes, the docs site picks them up on the next Mintlify build.

To vendor the spec instead (recommended pre-launch for stability), replace the URL with a relative path and check the spec file into `api-reference/openapi.json`.
