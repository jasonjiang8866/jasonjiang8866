# Jason Jiang

**ML Systems / AI Infrastructure**

I turn ML experiments into reproducible GPU workflows and working services into components other engineers can integrate. My background is in semiconductor manufacturing automation.

## Selected work

- **[waferVLM](https://github.com/jasonjiang8866/waferVLM)** — Wafer-map defect classification on the **same 160 validation maps**: DINOv3 LoRA **86.88%**, frozen DINOv3 + linear head **83.75%**, Qwen **78.13%**. **Evidence:** [full results](https://github.com/jasonjiang8866/waferVLM/blob/main/docs/dinov3-seed17-results.md) · [per-sample predictions and class probabilities](https://github.com/jasonjiang8866/waferVLM/blob/main/docs/showcase/dinov3-seed17/README.md#complete-predictions-and-probabilities). *Single-seed, validation-selected results—not an independent test or holdout evaluation.*

- **[FlashAttentionAnyCard](https://github.com/jasonjiang8866/flashattentionanycard)** — Reproducible Triton tuning for GEMM, RMSNorm, and grouped MoE. A real **PRO 6000 Blackwell MIG 24 GB** M0 run passed **19 GPU tests** and completed **18 tuning studies**; the temporary Pod was independently confirmed absent. **Evidence:** [M0 GPU run](https://github.com/jasonjiang8866/flashattentionanycard/actions/runs/43743010737) · [cleanup recovery](https://github.com/jasonjiang8866/flashattentionanycard/actions/runs/43743491986). *M0 is smoke/acceptance, not a performance benchmark. [M1 baselines and paired confirmation](https://github.com/jasonjiang8866/flashattentionanycard/pull/11) are in an open PR with offline CI; real GPU comparison and speedup claims remain pending.*

- **[smbfileserver](https://github.com/jasonjiang8866/smbfileserver)** — A reusable **Go SMB client**, embeddable standard **`net/http` handler**, and native gateway with **streaming-by-default HTTP/1.1+ single-file reads**, service authentication, and share/path access controls. **Evidence:** [real Samba + restricted-container CI](https://github.com/jasonjiang8866/smbfileserver/actions/runs/43739229025). *Client, handler, streaming, access controls, and deployment foundations are merged; [observability PR #9](https://github.com/jasonjiang8866/smbfileserver/pull/9) is open. Real OpenShift cluster acceptance is still pending.*

## More projects

- **[PEFT classification recipes](https://github.com/jasonjiang8866/peft-fine-tuning-recipes-classification)** — 8-bit Llama 3.2 LoRA text classification with a Muon/AdamW optimizer harness, [tested CPU Trainer/PEFT checkpoint resume](https://github.com/jasonjiang8866/peft-fine-tuning-recipes-classification/actions/runs/40272905969), and a pinned RunPod image; CUDA training and optimizer performance remain unverified.
- **[simplexLoRA-bench](https://github.com/jasonjiang8866/simplexLoRA-bench)** — Paired-seed LoRA / SimplexLoRA / DoRA GPU benchmarks with gradient diagnostics and archived lifecycle evidence.
- **[spleeterpt](https://github.com/jasonjiang8866/spleeterpt)** — Trainable PyTorch Spleeter port, converted official weights, and measured bounded-memory long-audio inference.
- **[runpod-ci-broker](https://github.com/jasonjiang8866/runpod-ci-broker)** — Budget-aware GPU experiment planning, read-only RunPod preflight, and fault-injection lifecycle simulation; general-purpose paid execution is not enabled.
