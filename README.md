# govagent-demo

A deliberately messy OpenAPI spec, used to demonstrate
[govagent](https://github.com/perrinstinct/govagent): an agent that finds API governance
violations deterministically, proposes verified JSON Patch fixes, and opens a pull request
with the fixes a human approved.

`openapi.yaml` breaks eight governance rules on purpose:

| Kind | Violations |
|---|---|
| Safe fixes | missing `summary` and `tags`, `http://` server URL, no 4xx response |
| Breaking fixes (explicit approval required) | camelCase path segment, snake_case `operationId`, PascalCase schema property |
| Needs a human | no contact email (business information the agent will not invent) |

The pull requests in this repository are opened by govagent.
