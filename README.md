# vendure-linui-bug-reporduction

## Setup

```bash
yarn install
yarn build
```

## Build Issue with Yarn

When running `yarn install` followed by `yarn build`, you may encounter a Lingui/Vite error:

```
[commonjs--resolver] The macro you imported from "@lingui/react/macro" is being executed outside the context of compilation.
```

**Cause:** The Angular UI devkit also uses Vite, which causes a Vite version mismatch when using yarn. This issue does not occur with npm. Removing the Angular UI component also resolves the issue.
