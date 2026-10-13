# Submissions

| Model | Public index | Results | Engine | Hardware | Settings and limits |
|---|---:|---|---|---|---|
| Lychee-27B ([`LycheeAI/Lychee-27B`](https://huggingface.co/LycheeAI/Lychee-27B) @ `f3f95d1`; decision model fine-tuned from Qwen3.8-27B, bf16, one forward pass per question, temperature 1.0) | **62.76** | [full run and scores](https://huggingface.co/datasets/LycheeAI/lychee-27b-decision-index/blob/cc17da8a52d258f591d492c6850a00797bf963e7/runs/lychee-27b/scores.json) | the kit's `http` engine (`model=lychee-27b`) against the model's bundled `/v1/systemone` server (`python -m lychee.server`), kit `f8552a1` (edition 0.3), unmodified runner, compact rows, 128 shards by sha256 of run id, concatenated | NVIDIA H100 80 GB, BF16, one server per GPU, one request at a time per server | prompts read whole up to 262,144 tokens; 1–255 options per choice; 2–10 score levels. |
