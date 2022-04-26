简体中文 | [English](/README.en-us.md)

<p align="center"><img alt="flow" src="/flow.svg"></p>

<p align="center"><strong>X6 是 AntV 旗下的图编辑引擎</strong></p>
<p align="center"><strong>提供简单易用的节点定制能力和开箱即用的交互组件，方便我们快速搭建流程图、DAG 图、ER 图等图应用</strong></p>

<p align="center">
<a href="https://github.com/antvis/X6/actions/workflows/ci.yml"><img alt="build" src="https://img.shields.io/github/workflow/status/antvis/x6/%F0%9F%91%B7%E3%80%80CI/master?logo=github&style=flat-square"></a>
<a href="https://app.codecov.io/gh/antvis/X6"><img alt="coverage" src="https://img.shields.io/codecov/c/gh/antvis/x6?logo=codecov&style=flat-square&token=15CO54WYUV"></a>
<a href="https://lgtm.com/projects/g/antvis/x6/context:javascript"><img alt="Language grade: JavaScript" src="https://img.shields.io/lgtm/grade/javascript/g/antvis/x6.svg?logo=lgtm&style=flat-square"></a>
<a href="https://www.npmjs.com/package/@antv/x6"><img alt="NPM Package" src="https://img.shields.io/npm/v/@antv/x6.svg?style=flat-square"></a>
<a href="https://www.npmjs.com/package/@antv/x6"><img alt="NPM Downloads" src="https://img.shields.io/npm/dm/@antv/x6?logo=npm&style=flat-square"></a>
</p>

<p align="center">
<a href="/LICENSE"><img src="https://img.shields.io/github/license/antvis/x6?style=flat-square" alt="MIT License"></a>
<a href="https://www.typescriptlang.org"><img alt="Language" src="https://img.shields.io/badge/language-TypeScript-blue.svg?style=flat-square"></a>
<a href="https://github.com/antvis/x6/pulls"><img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-Welcome-brightgreen.svg?style=flat-square"></a>
<a href="https://x6.antv.vision"><img alt="website" src="https://img.shields.io/static/v1?label=&labelColor=505050&message=website&color=0076D6&style=flat-square&logo=google-chrome&logoColor=0076D6"></a>
</p>

## 特性

- 🌱　极易定制：支持使用 SVG/HTML/React/Vue/Angular 定制节点样式和交互
- 🚀　开箱即用：内置 10+ 图编辑配套扩展，如框选、对齐线、小地图等
- 🧲　数据驱动：基于 MVC 架构，用户更加专注于数据逻辑和业务逻辑
- 💯　事件驱动：完备的事件系统，可以监听图表内发生的任何事件

## 兼容环境

- 现代浏览器和 IE11（需要 polyfills）
- 支持服务端渲染。

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)<br>Safari |
| --- | --- | --- | --- |
| IE11, Edge | last 2 versions | last 2 versions | last 2 versions |

## 安装

```shell
# npm
$ npm install @antv/x6 --save

# yarn
$ yarn add @antv/x6
```

## 示例

```html
<div id="container" style="width: 600px; height: 400px"></div>
```

```ts
import { Graph } from '@antv/x6'

const graph = new Graph({
  container: document.getElementById('container'),
  grid: true
})

const source = graph.addNode({
  x: 300,
  y: 40,
  width: 80,
  height: 40,
  label: 'Hello',
})

const target = graph.addNode({
  x: 420,
  y: 180,
  width: 80,
  height: 40,
  label: 'World',
})

graph.addEdge({
  source,
  target,
})
```

## 链接

- [文档](https://x6.antv.vision/zh/docs/tutorial/about)
- [示例](https://x6.antv.vision/zh/examples/gallery)
- [博客](https://www.yuque.com/antv/x6/gcinvi)
- [更新日志](https://www.yuque.com/antv/x6/bbfu6r)
- [常见问题](https://www.yuque.com/antv/x6/be9pfx)
- [CodeSanbox 模板](https://codesandbox.io/s/qosj0?file=/src/app.tsx)

## 本地开发

```shell
# 全局安装 yarn 和 lerna 工具
$ npm install yarn -g
$ npm install lerna -g

# 安装项目依赖和初始化构建
$ yarn bootstrap

# 进入到指定项目开发和调试
cd packages/x6
yarn build:watch

# 启动 example 查看效果
cd examples/x6-example-features
yarn start
```

## 参与共建

如果希望参与到 X6 的开发中，请遵从我们的[贡献指南](/CONTRIBUTING.zh-CN.md)。如果你贡献度足够活跃，你可以申请成为社区协作者。

<a href="https://github.com/antvis/x6/graphs/contributors">
  <img src="/CONTRIBUTORS.svg" alt="Contributors" width="740" />
</a>

## 开源协议

该项目的代码和文档基于 [MIT License](/LICENSE) 开源协议。