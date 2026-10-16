# notroela-engine

Prebuilt `whisper-cli` binaries (from [whisper.cpp](https://github.com/ggml-org/whisper.cpp))
for the [Notroela](https://github.com/ksipma/notroela) meeting recorder.

The Notroela app downloads these binaries on first use:

- `whisper-cli-win-x64.zip` — Windows x64, **Vulkan** (AMD Strix Halo iGPU supported)
- `whisper-cli-linux-x64.tar.gz` — Linux x64, **Vulkan**
- `whisper-cli-macos-arm64.tar.gz` — macOS Apple Silicon, **Metal**
- `whisper-cli-macos-x64.tar.gz` — macOS Intel, **Metal**

Binaries are statically linked (no extra runtime libs needed beyond the GPU
driver). CPU fallback is always compiled in.

## Rebuild

Trigger manually:

```bash
gh workflow run build.yml -f tag=v1
```

or via the GitHub Actions "Run workflow" button.