<p align="right">
  <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a>
</p>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="./assets/keelab-hero-light.svg" />
    <source media="(prefers-color-scheme: dark)" srcset="./assets/keelab-hero-dark.svg" />
    <img src="./assets/keelab-hero-dark.svg" width="100%" alt="Keelab：让复杂系统保持清晰边界" />
  </picture>
</div>

<p align="center">
  <a href="https://github.com/keelab/keelith"><img src="https://img.shields.io/badge/KEELITH-服务运行时-54e0d4?style=for-the-badge&labelColor=0b1724" alt="Keelith 服务运行时" /></a>
  <a href="https://github.com/keelab/keelmesh"><img src="https://img.shields.io/badge/KEELMESH-Agent%20执行循环-ffe0a3?style=for-the-badge&labelColor=0b1724" alt="Keelmesh Agent 执行循环" /></a>
  <a href="https://github.com/keelab/operator"><img src="https://img.shields.io/badge/KUBERNETES-拓扑治理-ff806e?style=for-the-badge&labelColor=0b1724" alt="Kubernetes 拓扑治理" /></a>
</p>

<p align="center">
  <a href="https://github.com/keelab">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=800&size=24&duration=2200&pause=720&color=54E0D4&center=true&vCenter=true&random=false&width=900&lines=%E6%98%8E%E7%A1%AE%E8%BE%B9%E7%95%8C%EF%BC%8C%E7%A8%B3%E5%AE%9A%E8%88%AA%E8%A1%8C;%E8%BF%90%E8%A1%8C%E6%97%B6%E8%BF%9B%EF%BC%8C%E7%B3%BB%E7%BB%9F%E8%BE%B9%E7%95%8C%E6%B8%85%E6%99%B0;%E6%90%AD%E5%BB%BA%E7%B3%BB%E7%BB%9F%E8%84%8A%E6%A2%81%EF%BC%8C%E4%BF%9D%E6%8C%81%E8%BE%B9%E7%95%8C%E6%98%8E%E7%A1%AE" alt="Keelab 打字机横幅" />
  </a>
</p>

<p align="center">
  <strong>开放系统，边界清晰。</strong><br />
  Keelab 面向分布式服务与 Agent 系统，围绕运行时、消息执行和发布治理构建可组合基础设施。
</p>

<p align="center"><code>意图 → 契约 → 运行时 → 信号 → 发布</code></p>

<div align="center">
  <img src="./assets/keelab-bridge.svg" width="100%" alt="Keelab 从运行时、服务网格到发布控制的项目桥" />
</div>

<br />

<details open>
  <summary><b>01 / 从这里开始</b></summary>

<table>
  <tr>
    <td width="33%" valign="top">
      <a href="https://github.com/keelab/keelith"><strong>keelith</strong></a><br />
      <sub>Go 运行时 · 生命周期 · DI · 传输 · 治理</sub><br /><br />
      面向分布式应用的生产级 Go 框架与 CLI。从这里搭起一条可运行、可诊断的服务边界。
    </td>
    <td width="33%" valign="top">
      <a href="https://github.com/keelab/keelmesh"><strong>keelmesh</strong></a><br />
      <sub>通道 · Agent · Gate · 执行循环</sub><br /><br />
      将消息、媒体、任务治理和执行编排放入清晰的进程边界，提供 HTTP/gRPC 与 Protobuf 接口。
    </td>
    <td width="33%" valign="top">
      <strong>keelway</strong><br />
      <sub>发布治理 · Kubernetes 优先 · 即将推出</sub><br /><br />
      发布治理轨道正在建设中：应用目录、不可变 Release、计划审批、执行、审计与恢复。
    </td>
  </tr>
</table>

<p>
  <a href="https://github.com/keelab/contrib"><strong>contrib</strong></a> · 外部基础设施适配<br />
  <a href="https://github.com/keelab/x"><strong>x</strong></a> · Hertz / Kitex 扩展传输<br />
  <a href="https://github.com/keelab/operator"><strong>operator</strong></a> · Kubernetes TopologyRevision 控制器<br />
  <a href="https://github.com/keelab/examples"><strong>examples</strong></a> · 从最小 HTTP 到拓扑控制的渐进示例
</p>

<p>
  <a href="https://github.com/keelab/keelith"><img src="https://img.shields.io/badge/从%20Keelith%20开始-0b1724?style=flat-square&logo=go&logoColor=54e0d4" alt="从 Keelith 开始" /></a>
  <a href="https://github.com/keelab?tab=repositories"><img src="https://img.shields.io/badge/查看全部仓库-54e0d4?style=flat-square&logo=github&logoColor=0b1724" alt="查看全部仓库" /></a>
</p>
</details>

<details>
  <summary><b>02 / 理解系统形态</b></summary>

<pre><code>意图 → 契约 → 组合 → 观测 → 演进</code></pre>

Keelab 不把复杂性藏在一层“神奇胶水”里，而是为每个重要边界命名、接线并留下信号：Keelith 承载服务运行时，Keelmesh 连接消息与 Agent，扩展模块接入基础设施，Keelway 负责把变更变成可审计的发布路径。

<pre><code>如果系统边界很重要，
它就应该被命名、可观测、可替换。</code></pre>

- **让业务代码保持普通。** 业务代码使用普通 Go / Rust；框架能力停在边界上。
- **让契约可执行。** 让 Proto、Binding、配置和发布意图可以生成、校验、回放。
- **把信号当作一等公民。** 日志、trace、metrics、审计与状态共同描述一次执行。
- **交付演进路径。** 交付可渐进启用的运行时、迁移和回滚路径，而不是孤立组件。

</details>

<details>
  <summary><b>03 / 运行第一个服务</b></summary>

从 Keelith 开始，几分钟内得到一个可运行的 HTTP 服务：

<pre><code>go install github.com/keelab/keelith/cmd/keelith@latest

keelith new hello
cd hello
go run .
# 另一个终端
curl http://127.0.0.1:8080/ping</code></pre>

| 目标 | 入口 |
| --- | --- |
| 构建服务 | <a href="https://github.com/keelab/keelith">keelith</a> 的 <code>new</code>、<code>add</code>、<code>wiring</code>、<code>doctor</code> |
| 连接消息与 Agent | <a href="https://github.com/keelab/keelmesh">keelmesh</a> 的 Channel / Agent / Gate / Loop |
| 接入外部系统 | <a href="https://github.com/keelab/contrib">contrib</a> 的 adapter 与 integration |
| 学习完整组合 | <a href="https://github.com/keelab/examples">examples</a> 的编号示例 |
| 管理 Kubernetes 拓扑 | <a href="https://github.com/keelab/operator">operator</a> 的 <code>TopologyRevision</code> |
</details>

<details>
  <summary><b>04 / 在开放中协作</b></summary>

Keelab 的公开仓库优先保持边界清晰、生成物可读、失败可诊断。项目仍在快速演进，升级前请查看各仓库的变更记录与迁移说明。

- <a href="https://github.com/keelab/keelith">Keelith 文档与 API</a>
- <a href="https://github.com/keelab/keelmesh">Keelmesh 文档</a>
- <a href="https://github.com/keelab/examples">Keelab 示例集合</a>
- <a href="https://github.com/keelab/keelith/blob/master/CONTRIBUTING.md">贡献指南</a>
- <a href="https://github.com/keelab/keelith/blob/master/SECURITY.md">安全政策</a>

Keelab 是一组开源系统项目；各仓库按项目分别授权，许可证与当前状态以对应仓库页面为准。
</details>

<p align="center"><sub>Keelab · build the spine, keep the edge explicit.</sub></p>
