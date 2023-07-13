# eurodata spectral rulesets

This project is based on the work of the following project [Github Project](https://github.com/baloise-incubator/spectral-ruleset) (Apache 2.0 licensed).

It provides two different rule sets:

* zalando
* eurodata

The eurodata rule set is based on the zalando by extending it.
It turns off certain zalando rules and replaces them with eurodata specific rules.

You can always be more strict than the `eurodata` ruleset.

The following `.spectral.yaml` (default rule file for a project) also includes the [OWASP API ruleset](https://github.com/stoplightio/spectral-owasp-ruleset)

The implemented rules can be seen the [source file](https://github.com/stoplightio/spectral-owasp-ruleset/blob/main/src/ruleset.ts)

```yaml
extends:
- ./eurodata.yml
- https://unpkg.com/@stoplight/spectral-owasp-ruleset/dist/ruleset.mjs

formats: [oas3]

rules:
must-use-problem-json-as-default-response: warn
```
