# homebridge-stack

Portainer Git stack for Homebridge on `apple-pi.lan`.

- **Stack name in Portainer:** `homebridge`
- **Config/state:** `/opt/homebridge` on the host (bind mount, ~357M). Not in this repo,
  not in any volume — back it up from the host.
- **UI:** http://apple-pi.lan:8581

## Version policy

Renovate checks for newer stable `YYYY-MM-DD` Homebridge Docker tags on Sunday
mornings Pacific time. The config excludes beta, legacy, and other named tags.
Review the release notes and plugin compatibility before merging an update PR.
Portainer polls the default branch every five minutes and deploys merged changes.

Rollback digest for 1.11.1: `sha256:653ac30...` (see vault AGENTS.md).
