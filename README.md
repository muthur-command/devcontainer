# Muthur Command Devcontainer

Custom devcontainers for use in Muthur Command OS repositories.


## Images

Image | Description | Dockerfile
-- | -- | --
`ghcr.io/muthur-command/devcontainer:apps` | For Muthur Command app development | [./apps/Dockerfile](./apps/Dockerfile)
`ghcr.io/muthur-command/devcontainer:supervisor` | For Supervisor development | [./supervisor/Dockerfile](./supervisor/Dockerfile)

Versioned images are available with the custom devcontainer version prepended (e.g. `4-supervisor`). This loosely resembles what upstream devcontainers provide as well. The version is meant to be incremented when non-backwards compatible changes are made. That allows existing devcontainer configuration to work while updating the devcontainers (e.g. when the Supervisor devcontainer is updated to a new Python version).

## Example files

Example files to use with Visual Studio Code

### Apps

Example files for the `apps` devcontainer

- [Example configuration (for `.devcontainer/devcontainer.json`)](./apps/devcontainer.json)
- [Example tasks file (for `.vscode/tasks.json`)](./apps/tasks.json)



## Notes

### `apps` and `supervisor`

- Use the command `supervisor_run` to start Muthur Command inside the devcontainer, or run the task "Start Muthur Command" if you copied the tasks file.
- Use `mc` to use the Muthur Command CLI (needs the supervisor to be running).

## Origin

- **Upstream:** [home-assistant/devcontainer](https://github.com/home-assistant/devcontainer) — upstream source repository (ported to Muthur Command OS).
- **In this repo:** **Muthur Command** keeps this copy for Muthur Command OS development; images and behavior may diverge from upstream over time.
- **License:** Code inherited from upstream remains **Apache-2.0**; see [`LICENSE`](./LICENSE).
