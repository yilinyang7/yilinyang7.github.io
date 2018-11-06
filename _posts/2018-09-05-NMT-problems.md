---
title: 'Well-Known Problems With Neural Machine Translation: Why RL Is The Future'
date: 2018-09-05
permalink: /posts/2018/
tags:
  - NMT
---

In addition to the *six challenges* listed in [1], here're the other well-known problems with Neural Machine Translation:

### Label Bias

Label bias was originally identified in HMMs and CRFs. And in the NMT literature, it mostly denotes the problem of *local normalization*. Since the baseline model of NMT [2,3] is trained with cross-entropy loss with teacher forcing, the loss is inevitably normalized on *locally* each step. Nowadays, several global training approaches have been adopted to solve this problem, e.g. Reinforcement Learning[4] and Minimal-Risk Training[5].

### Exposure Bias

Exposure bias denotes the problem that during decoding time, the model could reaches states where it hasn't been exposed in training time. Same as label bias, it's inevitable with local training with teacher forcing, and global training methods (i.e. RL, MRT) could alleviate this problem.

### Train/Test Evaluation Inconsistency

In the baseline of NMT systems [2,3], training loss is calculated by cross-entropy, while testing measurement are always non-differentiable metric (e.g. BLEU). Again, RL could solves this problem by calculating the loss directly from rewards (e.g. BLEU) it got from references. At the same time, an trial[6] to bring *brevity penalty* into log-likelihood is also intuitive for drawing connections between traditional model score with BLEU score.

**As a conclusion, RL method and other global training methods are the keys to solve above problems, and I think they are the future of NMT.**



### References:

1. Koehn, P., & Knowles, R. (2017). Six challenges for neural machine translation. *arXiv preprint arXiv:1706.03872*.
2. Bahdanau, D., Cho, K., & Bengio, Y. (2014). Neural machine translation by jointly learning to align and translate. *arXiv preprint arXiv:1409.0473*.
3. 4.Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., ... & Polosukhin, I. (2017). Attention is all you need. In *Advances in Neural Information Processing Systems*(pp. 5998-6008).
4. Ranzato, M. A., Chopra, S., Auli, M., & Zaremba, W. (2015). Sequence level training with recurrent neural networks. *arXiv preprint arXiv:1511.06732*.
5. Shen, S., Cheng, Y., He, Z., He, W., Wu, H., Sun, M., & Liu, Y. (2015). Minimum risk training for neural machine translation. *arXiv preprint arXiv:1512.02433*.
6. Yang, Y., Huang, L., & Ma, M. (2018). Breaking the Beam Search Curse: A Study of (Re-) Scoring Methods and Stopping Criteria for Neural Machine Translation. arXiv preprint arXiv:1808.09582.