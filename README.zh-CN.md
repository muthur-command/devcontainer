# Muthur Command Devcontainer

面向 **Muthur Command OS** 各仓库的自定义开发容器镜像。


## 镜像

镜像 | 说明 | Dockerfile
-- | -- | --
`ghcr.io/muthur-command/devcontainer:apps` | 开发 **App / Add-on** | [./apps/Dockerfile](./apps/Dockerfile)
`ghcr.io/muthur-command/devcontainer:supervisor` | 开发 **Supervisor** | [./supervisor/Dockerfile](./supervisor/Dockerfile)

带版本前缀的镜像同样可用（例如 `4-supervisor`），与上游 devcontainer 的版本策略类似。当出现不兼容变更时应递增版本号，以便各仓库在升级 devcontainer 的同时继续使用既有配置（例如 Supervisor devcontainer 升级 Python 版本时）。

## 示例文件

供 Visual Studio Code / Cursor 使用的示例配置

### Apps

`apps` devcontainer 示例：

- [示例 devcontainer 配置（`.devcontainer/devcontainer.json`）](./apps/devcontainer.json)
- [示例 tasks 文件（`.vscode/tasks.json`）](./apps/tasks.json)



## 使用说明

### `apps` 与 `supervisor`

- 运行 `supervisor_run` 在 devcontainer 内启动 Muthur Command；若已复制 tasks 文件，也可执行 **Start Muthur Command** 任务。
- 运行 `mc` 使用 Muthur Command CLI（需 Supervisor 已运行）。

## 来源

- **上游：** [home-assistant/devcontainer](https://github.com/home-assistant/devcontainer) — 上游来源仓库（移植至 Muthur Command OS）。
- **本仓库：** **Muthur Command** 在本文档所在仓库维护该副本，供 **Muthur Command OS** 开发使用；镜像与行为可能随时间与上游产生差异。
- **许可：** 自上游继承的代码仍为 **Apache-2.0**；见 [`LICENSE`](./LICENSE)。
