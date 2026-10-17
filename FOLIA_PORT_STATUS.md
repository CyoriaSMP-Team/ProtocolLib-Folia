# ProtocolLib compatibility: Folia 1.21.11

This fork is retained as a workspace for **source changes only if upstream requires them**. Source was forked directly from [`dmulloy2/ProtocolLib`](https://github.com/dmulloy2/ProtocolLib), not from an unofficial fork. No unofficial scheduler patch has been applied to this branch.

## Tested official artifact

- Official GitHub `dev-build` release, asset `ProtocolLib-Spigot.jar`, internal `5.5.0-SNAPSHOT` (release asset hash is verified locally on the CyoriaSMP host).
- Descriptor `plugin.yml` advertises `folia-supported: true` and `api-version: 1.13`. The companion `ProtocolLib.jar` Paper descriptor advertises `api-version: 26.2`, so **do not install that asset on Folia 1.21.11**.
- Isolated Folia 1.21.11-14 smoke tests loaded `ProtocolLib-Spigot.jar` on its own and with the official Folia builds of AuthMe 6.0.1 + FastLoginPlus 0.7.0. Both staging instances reached server startup completion without a ProtocolLib loading failure.
- CyoriaSMP loaded it and reached `Done`, while FastLoginPlus detected AuthMe and registered the configure-phase authentication flow.

## Not yet verified

- A real user joining with Java Premium, Java Offline and Bedrock via Floodgate.
- Packet interception from multiple Folia regions concurrently, ping handling and live packet protocol semantics.
- Upstream Paper variant `api-version 26.2` cannot load on 1.21.11; do not weaken metadata to bypass its minimum API.

Official binary is currently preferred. No automatic merge or server deployment is configured for this fork.
