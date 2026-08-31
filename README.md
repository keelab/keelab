<p align="right">
  <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a>
</p>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="./assets/keelab-hero-light.svg" />
    <source media="(prefers-color-scheme: dark)" srcset="./assets/keelab-hero-dark.svg" />
    <img src="./assets/keelab-hero-dark.svg" width="100%" alt="Keelab: clear boundaries for complex systems" />
  </picture>
</div>

<p align="center">
  <a href="https://github.com/keelab/keelith"><img src="https://img.shields.io/badge/KEELITH-SERVICE%20RUNTIME-54e0d4?style=for-the-badge&labelColor=0b1724" alt="Keelith service runtime" /></a>
  <a href="https://github.com/keelab/keelmesh"><img src="https://img.shields.io/badge/KEELMESH-AGENT%20LOOPS-ffe0a3?style=for-the-badge&labelColor=0b1724" alt="Keelmesh agent loops" /></a>
  <a href="https://github.com/keelab/operator"><img src="https://img.shields.io/badge/KUBERNETES-TOPOLOGY-ff806e?style=for-the-badge&labelColor=0b1724" alt="Kubernetes topology" /></a>
</p>

<p align="center">
  <strong>Open systems. Explicit boundaries.</strong><br />
  Keelab builds composable infrastructure for distributed services and agent systems, centered on runtime, message execution, and release governance.
</p>

<p align="center"><code>intent → contract → runtime → signal → release</code></p>

<div align="center">
  <img src="./assets/keelab-bridge.svg" width="100%" alt="Keelab project bridge from runtime and mesh to release control" />
</div>

<br />

<details open>
  <summary><b>01 / Find your starting point</b></summary>

<table>
  <tr>
    <td width="33%" valign="top">
      <a href="https://github.com/keelab/keelith"><strong>keelith</strong></a><br />
      <sub>Go runtime · lifecycle · DI · transport · governance</sub><br /><br />
      A production-oriented Go framework and CLI for distributed applications. Start here to build a service boundary that runs and diagnoses clearly.
    </td>
    <td width="33%" valign="top">
      <a href="https://github.com/keelab/keelmesh"><strong>keelmesh</strong></a><br />
      <sub>channels · agents · gates · execution loops</sub><br /><br />
      Put messages, media, task governance, and execution orchestration behind clear process boundaries with HTTP/gRPC and Protobuf interfaces.
    </td>
    <td width="33%" valign="top">
      <strong>keelway</strong><br />
      <sub>release governance · Kubernetes-first · coming soon</sub><br /><br />
      The release governance track is taking shape: application catalogs, immutable releases, plan approval, execution, audit, and recovery.
    </td>
  </tr>
</table>

<p>
  <a href="https://github.com/keelab/contrib"><strong>contrib</strong></a> · external infrastructure adapters<br />
  <a href="https://github.com/keelab/x"><strong>x</strong></a> · Hertz / Kitex transport extensions<br />
  <a href="https://github.com/keelab/operator"><strong>operator</strong></a> · Kubernetes TopologyRevision controller<br />
  <a href="https://github.com/keelab/examples"><strong>examples</strong></a> · progressive examples from minimal HTTP to topology control
</p>

<p>
  <a href="https://github.com/keelab/keelith"><img src="https://img.shields.io/badge/Start%20with%20Keelith-0b1724?style=flat-square&logo=go&logoColor=54e0d4" alt="Start with Keelith" /></a>
  <a href="https://github.com/keelab?tab=repositories"><img src="https://img.shields.io/badge/View%20all%20repositories-54e0d4?style=flat-square&logo=github&logoColor=0b1724" alt="View all repositories" /></a>
</p>
</details>

<details>
  <summary><b>02 / Trace the system shape</b></summary>

<pre><code>intent → contract → compose → observe → evolve</code></pre>

Keelab does not hide complexity behind a layer of “magic glue.” It names, wires, and signals every important boundary: Keelith carries the service runtime, Keelmesh connects messages and agents, extensions connect infrastructure, and Keelway turns changes into an auditable release path.

<pre><code>If a system boundary matters,
it should be named, observable, and replaceable.</code></pre>

- <strong>Keep business code ordinary.</strong> Use ordinary Go / Rust for business code; keep framework capabilities at the boundary.
- <strong>Make contracts executable.</strong> Generate, validate, and replay Proto, bindings, configuration, and release intent.
- <strong>Treat signals as first-class.</strong> Logs, traces, metrics, audits, and state describe an execution together.
- <strong>Ship evolution paths.</strong> Deliver runtimes, migrations, and rollback paths that can be enabled progressively, not isolated components.

</details>

<details>
  <summary><b>03 / Run the first service</b></summary>

Start with Keelith and get a runnable HTTP service in minutes:

<pre><code>go install github.com/keelab/keelith/cmd/keelith@latest

keelith new hello
cd hello
go run .
# in another terminal
curl http://127.0.0.1:8080/ping</code></pre>

Choose a path based on your goal:

| Goal | Entry point |
| --- | --- |
| Build a service | <a href="https://github.com/keelab/keelith">keelith</a> <code>new</code>, <code>add</code>, <code>wiring</code>, and <code>doctor</code> |
| Connect messages and agents | <a href="https://github.com/keelab/keelmesh">keelmesh</a> Channel / Agent / Gate / Loop |
| Integrate external systems | <a href="https://github.com/keelab/contrib">contrib</a> adapters and integrations |
| Learn the full composition | Numbered examples in <a href="https://github.com/keelab/examples">examples</a> |
| Manage Kubernetes topology | <code>TopologyRevision</code> in <a href="https://github.com/keelab/operator">operator</a> |

<p>
  <a href="https://pkg.go.dev/github.com/keelab/keelith"><img src="https://img.shields.io/badge/API%20reference-pkg.go.dev-54e0d4?style=flat-square&logo=go&logoColor=0b1724" alt="API reference" /></a>
  <a href="https://github.com/keelab/keelith/blob/master/CONTRIBUTING.md"><img src="https://img.shields.io/badge/Contribute-read%20the%20guide-ffe0a3?style=flat-square&logo=github&logoColor=0b1724" alt="Contributing guide" /></a>
</p>
</details>

<details>
  <summary><b>04 / Work in the open</b></summary>

Keelab's public repositories prioritize clear boundaries, readable generated artifacts, and diagnosable failures. The projects are evolving quickly; review each repository's changelog and migration notes before upgrading.

- <a href="https://github.com/keelab/keelith">Keelith docs and API</a>
- <a href="https://github.com/keelab/keelmesh">Keelmesh docs</a>
- <a href="https://github.com/keelab/examples">Keelab examples</a>
- <a href="https://github.com/keelab/keelith/blob/master/CONTRIBUTING.md">Contributing guide</a>
- <a href="https://github.com/keelab/keelith/blob/master/SECURITY.md">Security policy</a>

<p align="center">
  <img src="./assets/keelith-avatar.png" width="112" alt="Keelith mascot" />
</p>

Keelab is a set of open-source systems projects. Each repository is licensed independently; see its repository page for the current license and status.
</details>

<p align="center">
  <sub>Keelab · build the spine, keep the edge explicit.</sub>
</p>
