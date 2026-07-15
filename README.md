# Slide in Sync Remix Runtime

Public, versioned Defold runtime artifacts used by the Remix build of
**Slide in Sync**.

## Releases

- `v0.0.1`: external-loading probe only.
- `v0.1.0`: first production candidate with the Defold WASM engine and game
  archive under `runtime/`.

The Remix HTML shell loads `v0.1.0` from this immutable jsDelivr base:

```text
https://cdn.jsdelivr.net/gh/lhyisboss/slide-in-sync-remix-runtime@v0.1.0/runtime/
```

Every hosted file is listed with its byte size and SHA-256 digest in
`runtime/runtime-manifest.json`. Production consumers must pin an immutable tag
or commit; do not use `main` or `latest` URLs.
