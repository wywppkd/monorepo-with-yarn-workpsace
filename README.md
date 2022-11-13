```bash
yarn workspaces info # 展示所有包及其依赖
yarn workspace package-a add react@17 # 给 a 包安装依赖
yarn workspace package-a add typescript --dev # 给 a 包安装开发依赖
yarn workspace package-a add package-b # 给 a 包安装开发依赖
yarn workspaces run build # 执行每个 packages 的 script(yarn run build) 命令
yarn workspace package-a run build # 执行每个 package-a 的 script(yarn run build) 命令
  # PS: 也可以切换到 package-a 目录, 然后执行 yarn run build
```

## package-a 依赖 package-b

- 手动修改 package-a 的 pkg

```js
// package-a/package.json
{
  // ...
  "dependencies": {
    "package-b": "1.0.0"
  }
}
```

