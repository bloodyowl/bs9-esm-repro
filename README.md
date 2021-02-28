## BS9/esm bug

```
node -r esm src/demo.bs.js
```

gives you a `ERR_REQUIRE_ESM`

```
bs9-esm-repro/node_modules/bs-platform/lib/es6/caml_option.js:1
Error [ERR_REQUIRE_ESM]: Must use import to load ES Module: bs9-esm-repro/node_modules/bs-platform/lib/es6/caml_option.js
require() of ES modules is not supported.
require() of bs9-esm-repro/node_modules/bs-platform/lib/es6/caml_option.js from bs9-esm-repro/src/demo.bs.js is an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which defines all .js files in that package scope as ES modules.
Instead rename caml_option.js to end in .cjs, change the requiring code to use import(), or remove "type": "module" from bs9-esm-repro/node_modules/bs-platform/lib/es6/package.json.
```