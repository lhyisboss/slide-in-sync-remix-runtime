# Slide in Sync Remix Runtime

Public, versioned Defold runtime artifacts used by the Remix build of
**Slide in Sync**.

## Releases

- `v0.0.1`: external-loading probe only.
- `v0.1.0`: first production candidate with the Defold WASM engine and game
  archive under `runtime/`.
- `v0.2.0`: Remix-safe script transport. The engine and archive are Zstandard
  compressed inside `runtime-data.js`, decoded in memory, and never requested
  with `fetch` or `XMLHttpRequest`.

The Remix HTML shell loads `v0.2.0` from this immutable jsDelivr base:

```text
https://cdn.jsdelivr.net/gh/lhyisboss/slide-in-sync-remix-runtime@v0.2.0/runtime/
```

The page loads only `runtime-data.js` and `dmloader.js` as static scripts.
`runtime/runtime-manifest.json` records source and hosted sizes plus SHA-256
digests. Production consumers must pin an immutable tag or commit; do not use
`main` or `latest` URLs.
