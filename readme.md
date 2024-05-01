# monorepo

## 内容
pnpm-workspace.yaml
- packages
  - react-demo
  - vue3-demo

## 初始化
如果你是项目创建者
1. pnpm init 全局项目
2. 自己创建 `pnpm-workspace.yaml` 文件并配置包含 `packages`
3. 自己创建两个项目， `react-demo` 和 `vue3-demo`。进去一个个的`pnpm init` （pnpm无法通过`--filter react-demo init` 在根部就帮助初始化）
4. 有共同的npm包，就用`pnpm add [module-name] -w` （-w == --workspace-root）
5. 各项目独立的包， 就 `pnpm --filter [packageName] add [module-name] -S`

如果该项目已经创建，你只是拉下来
1. 直接安装依赖即可 `pnpm install`。 pnpm会帮忙一键安装workspace-root的依赖以及各个packages内部的依赖