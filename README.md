# Jason Jiang

**ML Systems / AI Infrastructure**

I turn ML experiments into reproducible GPU workflows and working services into components other engineers can integrate. My background is in semiconductor manufacturing automation.

## Selected work

- **[waferVLM](https://github.com/jasonjiang8866/waferVLM)** — On the same 160 validation maps, DINOv3 vision LoRA improved wafer defect classification accuracy over a frozen backbone with a linear head by **3.75, 5.00 and 5.00 percentage points** (training seeds 17, 42 and 123). The six models produced 2,880 validation predictions across 18 processes. The separate 148-map unseen-lot holdout still has **0 of 888 planned predictions**. [Paired validation results](https://github.com/jasonjiang8866/waferVLM/blob/main/docs/dinov3-confirmation-results.md)

- **[FlashAttentionAnyCard](https://github.com/jasonjiang8866/flashattentionanycard)** — Tunes Triton GEMM, RMSNorm and grouped MoE kernels against PyTorch baselines. On a 24 GB RTX PRO 6000 Blackwell MIG slice, the M1 smoke run passed **25 GPU tests** and retested 18 selected configurations in 108 paired runs on synthetic inputs. [M1 GPU acceptance](https://github.com/jasonjiang8866/flashattentionanycard/actions/runs/43917307722)

- **[smbfileserver](https://github.com/jasonjiang8866/smbfileserver)** — A Go SMB client and embeddable `net/http` handler for streaming files, with an authenticated gateway that enforces share and path restrictions. CI verifies real Samba reads and restricted-container execution. OpenShift cluster acceptance is pending. [Samba and container CI](https://github.com/jasonjiang8866/smbfileserver/actions/runs/43739229025)

## More projects

- **[PEFT classification recipes](https://github.com/jasonjiang8866/peft-fine-tuning-recipes-classification)** — Tested checkpoint recovery for Qwen3.5-0.8B text classification on an RTX 4090. AdamW and Muon each resumed from step 6 and matched uninterrupted training at step 12 (maximum absolute tensor difference **0** for both). The 105-minute allocation expired before the 200-step optimizer comparison finished. [CUDA smoke and timeout](https://github.com/jasonjiang8866/peft-fine-tuning-recipes-classification/actions/runs/44411232628)
- **[MLsysZero2Hero](https://github.com/jasonjiang8866/MLsysZero2Hero)** — Bilingual ML systems labs. E00 ran an FP32 vector-add kernel on an RTX 4090, collected the result, verified the GitHub artifact receipt and confirmed Pod deletion. [E00 acceptance run](https://github.com/jasonjiang8866/MLsysZero2Hero/actions/runs/44523422041)
- **[MiniMind zh2en agent](https://github.com/jasonjiang8866/minimind-zh2en-agent)** — LangGraph translates, validates and corrects text through a local vLLM endpoint. A draft PR adds [resumable batch processing](https://github.com/jasonjiang8866/minimind-zh2en-agent/pull/7) with [mock-HTTP tests](https://github.com/jasonjiang8866/minimind-zh2en-agent/actions/runs/40533729630).
- **[simplexLoRA-bench](https://github.com/jasonjiang8866/simplexLoRA-bench)** — Paired-seed LoRA / SimplexLoRA / DoRA GPU benchmarks with gradient diagnostics and archived lifecycle evidence.
- **[spleeterpt](https://github.com/jasonjiang8866/spleeterpt)** — Trainable PyTorch Spleeter port, converted official weights, and measured bounded-memory long-audio inference.
- **[runpod-ci-broker](https://github.com/jasonjiang8866/runpod-ci-broker)** — Finds GPU capacity within a task’s budget and hardware limits. Its RTX 4090 CUDA memory smoke verified result upload and Pod deletion, followed by an independent cleanup check. [Run and recovery evidence](https://github.com/jasonjiang8866/runpod-ci-broker/pull/31)
