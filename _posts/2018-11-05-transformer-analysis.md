---
title: 'Granular Analysis of Transformer'
date: 2018-11-05
permalink: /posts/2018/transformer-analysis
tags:
  - NMT
---

I want to write this blog to save some widely observed conclusions with Transformer Network [1]:

1. Decoder-to-encoder attention on the top encoder layer leverages the best performance, compared to increasing or decreasing order of decoder-to-encoder attention.
2. Multiple decoder-to-encoder attention layers (decoder-to-encoder attenion is embedded into every decoder layer) is crucial to the performance (+1.2 BLEU), while multi-head decoder-to-encoder attention is not that important (+0.3 BLEU).
3. Residual feed-forward layers in each encoder/decoder layer are also keys to the performance (+1.2 BLEU)
4. Self-attention is more important for the source than for the target side. The transformer decoder could generally be substituted by RNN/CNN decoder with no worse performance.

The above conclusions are firstly observed in [2], then also implemented in RNMT+ [3], while RNMT+ preserves both the transformer encoder and decoder-to-encoder attention, and substitute the decoder with RNN decoder and get a higher BLEU score. 

Another line of works only use transformer encoder: [4] utilizes only the transformer encoder as a better feature extractor on span-based constituency parsing model; BERT [5] use the transformer encoder to pretrain bidirectional (important!) language model and next-sentence prediction tasks, and achieve STOA on plenty of downstream tasks with additional fine-tune training.



### References:

1. Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., ... & Polosukhin, I. (2017). Attention is all you need. In *Advances in Neural Information Processing Systems*(pp. 5998-6008).
2. Domhan, T. (2018). How much attention do you need? a granular analysis of neural machine translation architectures. In *Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)* (Vol. 1, pp. 1799-1808).
3. Chen, M. X., Firat, O., Bapna, A., Johnson, M., Macherey, W., Foster, G., ... & Wu, Y. (2018). The Best of Both Worlds: Combining Recent Advances in Neural Machine Translation. *arXiv preprint arXiv:1804.09849*.
4. Kitaev, N., & Klein, D. (2018). Constituency Parsing with a Self-Attentive Encoder. *arXiv preprint arXiv:1805.01052*.
5. Devlin, J., Chang, M. W., Lee, K., & Toutanova, K. (2018). BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. *arXiv preprint arXiv:1810.04805*.