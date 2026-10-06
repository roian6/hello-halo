# Halo #384 renderer evidence

These images show the actual StoreDetail component with deterministic injected local data and an observed-state panel, not a full application destination. SpacePage and InputArea are not mounted. Background API, translation and passive presentation surfaces are mocked; no real Halo account, user data, credentials or install lifecycle is shown.

The before build contains the original StoreDetail from main d4314a495d0cc9958976b7b50ea43d9a9c53a738. The after build contains the fix at 600c12f6ae0019bb23c4aed053343e45a177db8c. Source-map contents were compared with both actual source files.

- fresh-global: a global skill with no current/custom space; before currentSpace and pending input are null, after Halo is selected and `/demo-skill ` is queued.
- fresh-halo: an explicitly Halo-installed skill with no current/custom space at 390px; before currentSpace and pending input are null, after Halo is selected and `/demo-skill ` is queued.
- halo-current-custom: an explicitly Halo-installed skill while a custom space is current; before the custom space is used, after Halo is selected and `/demo-skill ` is queued for Halo.

The existing isolated runtime uses React/ReactDOM 19.2.7, Zustand 5.0.14, Chromium 152.0.7977.82 and Node 26.6.0. Halo's React 18/Zustand 4 and Electron runtime are not validated. Nine before/after component scenarios passed their respective expected-behavior assertions; Hermes independently repeated the three defect paths after the fix.

This is a standalone media branch in the contributor fork, not a change to the code PR or fork main. No native fresh-install, full app routing, composer consumption, background refresh success, or full project build is claimed.
