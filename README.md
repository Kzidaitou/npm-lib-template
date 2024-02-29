# npm-lib-template

本人用于编写的一个 `npm` 包的一个模板

- 使用 `rollup` 打包 (兼容 `tsc`)
- 使用 ~~`jest`~~ `vitest` 作为单元测试框架
- 使用 `eslint` 来规范代码风格，默认风格为 `standard`
- 输出 `dist` -> `cjs`,`esm` and `.d.ts`
- 使用 `semantic-release` 来发布 `npm`/`github`

## 为什么使用 `vitest` 而不是原先的 `jest`

`vitest` 开箱即用,`jest` 在同时遇到 `cjs` 和 `esm` 依赖的时候，支持很差，经常会失败，而且配置复杂，依赖的 `preset` 多，比如 `ts-jest`..

## scripts

### rename

执行 `npm run init:rename`

作用为替换 `package.json` 中默认包含的所有名称为 `npm-lib-template` 的字段

默认替换为新建代码仓库的文件夹名称！

### bin

执行 `npm run init:bin`

作用为 `package.json`  添加 `files` 和 `bin`，同时生成 `bin/{{pkg.name}}.js` 和 `src/cli.ts` 文件

## Git 提交规范

- `feat` 新功能
- `fix` 修补 bug
- `docs` 文档
- `style` 格式、样式(不影响代码运行的变动)
- `refactor` 重构(即不是新增功能，也不是修改 BUG 的代码)
- `perf` 优化相关，比如提升性能、体验
- `test` 添加测试
- `build` 编译相关的修改，对项目构建或者依赖的改动
- `ci` 持续集成修改
- `chore` 构建过程或辅助工具的变动
- `revert` 回滚到上一个版本
- `workflow` 工作流改进
- `mod` 不确定分类的修改
- `wip` 开发中
- `types` 类型