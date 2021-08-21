# Gentype Module Bug


## Build
This repository include pre-built files.

```
$ npm i -ws
$ npm run -w module-a build
$ npm run -w module-b build
```

## Bug details
[packages/module-b/src/Bar.gen.tsx#L9](https://github.com/kgtkr/typegen-module-bug/blob/master/packages/module-b/src/Bar.gen.tsx#L9)
output: `import type {Foo_t as ModuleA_Foo_t} from 'module-a/ModuleA.gen';`
expect: `import type {t as ModuleA_Foo_t} from 'module-a/Foo.gen';`
