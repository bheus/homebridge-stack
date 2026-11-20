# homebridge-stack

Portainer Git stack for Homebridge on `apple-pi.lan`.

- **Stack name in Portainer:** `homebridge`
- **Config/state:** `/opt/homebridge` on the host (bind mount, ~357M). Not in this repo,
  not in any volume — back it up from the host.
- **UI:** http://apple-pi.lan:8581

## Version policy

Homebridge publishes **dated tags only** (`2026-11-15`), not semver, so Dependabot and
Renovate can't parse them without a custom versioning rule. This image is therefore
**updated manually and deliberately** — majors break plugins.

To update: check https://hub.docker.com/r/homebridge/homebridge/tags, read the release
notes, bump the tag here, and let Portainer redeploy (5-minute poll).

Rollback digest for 1.11.1: `sha256:653ac30...` (see vault AGENTS.md).
