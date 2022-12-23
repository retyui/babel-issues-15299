To reproduce https://github.com/babel/babel/issues/15299

```sh
# clone this repo
yarn install
yarn list @babel/traverse # 7.20.8

npx react-native bundle --platform ios --dev true --entry-file index.js --bundle-output ./bundle.txt

# error node_modules/react-hook-form/dist/index.cjs.js: /babelIssues/node_modules/react-hook-form/dist/index.cjs.js: Cannot read properties of null (reading 'scope').
# TypeError: /babelIssues/node_modules/react-hook-form/dist/index.cjs.js: Cannot read properties of null (reading 'scope')
```

