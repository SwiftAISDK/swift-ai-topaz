# Changelog

## 1.1.0

- Add native async throwing apiKeyProvider; resolve a fresh key immediately before every authenticated HTTP send/stream through the shared transport. Preserve static keys, custom header precedence, error/abort propagation, request builders and response parsers. Submit and each authenticated poll refresh credentials. Existing JSON accept headers and unauthenticated output download behavior are preserved. Reviewed upstream: @ai-sdk/topaz 3.0.15 to 3.0.19. Validation passed: node Scripts/test-packages.mjs (all 52 owning package suites and the compatibility facade); node Scripts/sdk.mjs generate --check; node --test Scripts/tests/*.test.cjs (27 passed); docs-site check and build (100 pages). Live provider calls were not run.
  Compatibility: Minor release for additive native API; existing static settings and call sites remain compatible. Updated direct dependency minimums are recorded in the manifest. Existing documented JS/framework and native product gaps remain; version-delta review does not imply full parity or live-service testing. Explicit custom authentication skips an unused credential supplier, a deliberate native callback-order adaptation.
