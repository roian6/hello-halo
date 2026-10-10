# Halo issue #426: browser-data control evidence

Six unchanged PNG captures from isolated Linux ARM64 Electron 43.7.7 profiles.

- Before implementation: release_v3 source `ee81f14d80bc765dfff02acfd9970a0d73caadc7`.
- After implementation and locale generation: source tree `ea5b7b117ed0c76761c48bfce39b72d3f5665b21`.
- Desktop: 1280 x 900. Narrow view: 540 x 900.
- Confirmation warns about all shared-browser site logins and digital humans, preserves Halo data and other browser sessions.
- After-cleanup captures show the actual Settings success state. A confirmation does not show a completed new operation.
- No real personal account/profile or live SSO provider was used. Any loopback proxy value is an app default in the isolated test profile.

This evidence branch is separate from the feature PR, so screenshot binaries are not added to upstream source history.
