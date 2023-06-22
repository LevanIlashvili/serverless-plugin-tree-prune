# serverless-plugin-tree-prune

Based on [serverless-plugin-tree-shake](https://github.com/sergioramos/serverless-plugin-tree-shake)

Shake the file dependency tree and only include files needed.

## install

```bash
yarn add --dev serverless-plugin-tree-prune
```

```bash
npm install --save-dev serverless-plugin-tree-prune
```

## usage

```yaml
plugins:
  - serverless-plugin-tree-prune
package:
  excludeDevDependencies: false
```

This plugins supports typescript natively. It uses the installed typescript package, reads the appropriate config, and transpiles to js according to that config. You can see examples on the [`__fixtures__`](./test/__fixtures__) that start with `ts-`.

##### individually

This plugins supports bundling functions `individually`. Just use that option accordingly:

```yaml
package:
  individually: true
  excludeDevDependencies: false
```
