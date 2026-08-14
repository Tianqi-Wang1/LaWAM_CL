---
license: mit
pipeline_tag: robotics
---

# dino_large_vae LaWAM Release

This directory is the minimal release package needed by LaWAM training.

This model is part of the work presented in the paper [LaWAM: Latent World Action Models for Efficient Dynamics-Aware Robot Policies](https://huggingface.co/papers/2606.15768).

- **Project Page:** [https://rlinf.github.io/LaWAM/](https://rlinf.github.io/LaWAM/)
- **GitHub Repository:** [https://github.com/RLinf/LaWAM](https://github.com/RLinf/LaWAM)

## Kept files:

- `dino_large_vae.yaml`: LAM model configuration consumed by `lam_yaml_path`.
- `checkpoints/pytorch_model.pt`: LAM release checkpoint consumed by
  `lam_ckpt_path`. It keeps only the `state_dict` needed by LaWAM training and
  inference.

## Example LaWAM config:

```yaml
framework:
  action_model:
    lam_ckpt_path: "latent_action_model/logs/dino_large_vae/lam_release/checkpoints/pytorch_model.pt"
    lam_yaml_path: "latent_action_model/logs/dino_large_vae/lam_release/dino_large_vae.yaml"
```

## Citation

```bibtex
@misc{chen2026lawam,
  title = {LaWAM: Latent World Action Models for Efficient Dynamics-Aware Robot Policies},
  author = {Chen, Jialei and Wang, Kai and Chen, Kang and Chen, Shuaihang and Gao, Feng and Tang, Wenhao and Li, Zhiyuan and Liu, Weilin and Yao, Zhuyu and Li, Boxun and Xu, Yuanbo and Yu, Chao},
  journal = {arXiv preprint arXiv:2606.15768},
  year = {2026},
  archiveprefix = {arXiv},
  primaryclass = {cs.RO},
}
```