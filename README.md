# SenseNova Colab

Prebuilt `llama-server` for [SenseNova-Loop-9B-abliterated-GGUF](https://huggingface.co/satellitedown/SenseNova-Loop-9B-abliterated-GGUF),
built from [GuideboardLabs/llama.cpp-sensenova-loop](https://github.com/GuideboardLabs/llama.cpp-sensenova-loop)
at `a7f77a7` with the 18 SenseNova patches, CUDA 13.0, `sm_75` (Tesla T4 class).

## Download

[SenseNova-llama-server-cuda-sm75.zip](https://github.com/GodL-x-SouL/SenseNova-Colab/releases/latest/download/SenseNova-llama-server-cuda-sm75.zip) (~146 MB)

Contains `llama.cpp-loop/build/bin/` — `llama-server` plus its shared libraries.

## Restore

```bash
mkdir -p /content/SenseNovaLoop && cd /content/SenseNovaLoop
unzip -o SenseNova-llama-server-cuda-sm75.zip
```

The notebook's cell 01 downloads and unpacks this release automatically.

## Notes

- Built binaries embed RUNPATHs to `/content/SenseNovaLoop/llama.cpp-loop/build/bin`,
  so restore into that exact location.
- Needs the same Colab image family (CUDA 13.x, glibc) and an `sm_75` GPU (T4);
  on a different GPU or image, rebuild from source.
