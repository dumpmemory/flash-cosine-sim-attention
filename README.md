## Flash Cosine Similarity Attention (wip)

Implementation of fused cosine similarity attention in the same style as <a href="https://arxiv.org/abs/2205.14135">Flash Attention</a>. The observation is that by adopting l2 normalized queries and keys, you no longer need to keep track of the row maximums for numerical stability. This greatly simplifies the flash attention algorithm, assuming cosine similarity attention comes at no generalization cost.

In other words, stable, fast, memory efficient, and longer context attention with no downsides.

This will be my first attempt at CUDA, so welcome any help or advice.

## Citations

```bibtex
@article{Dao2022FlashAttentionFA,
    title   = {FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness},
    author  = {Tri Dao and Daniel Y. Fu and Stefano Ermon and Atri Rudra and Christopher R'e},
    journal = {ArXiv},
    year    = {2022},
    volume  = {abs/2205.14135}
}
```

```bibtex
@inproceedings{Henry2020QueryKeyNF,
    title   = {Query-Key Normalization for Transformers},
    author  = {Alex Henry and Prudhvi Raj Dachapally and Shubham Vivek Pawar and Yuxuan Chen},
    booktitle = {FINDINGS},
    year    = {2020}
}
```
