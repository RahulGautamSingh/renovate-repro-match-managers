# matchManagers validation repro

`packageRules[0].matchManagers` uses `"jsonata"` (should be `"custom.jsonata"`) and the typo `"npmm"`. Neither matches any manager, and validation currently accepts the config without an error.

```sh
npx --package renovate renovate-config-validator renovate.json
```
