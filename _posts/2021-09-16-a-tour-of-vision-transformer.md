## A tour of Vision Transformer

### Motivation
I find Vision Transformer interesting for we were working on some small object detection project.
I started from the popular DETR, ViT, Swin Transformer, Deformable, etc, I learned quite a lot from reading the papers and source code.
Hence, I plan to write down what I learned first to improve my technical writing skills, 
second to share knowledge and reflections with people who's sharing similar interests.

### 1. From Self-attention - "Attention Is All You Need"
Transformer is a sequence to sequence model, 
and for the sequence modeling the most common model is RNN.

Recurrent models typically factor computation along the symbol positions of the input and output sequences. 
Aligning the positions to steps in computation time, they generate a sequence of hidden states `h_t`, 
as a function of the previous hidden state \\( h_{t−1} \\) and the input for position t. 
This inherently sequential nature precludes parallelization within training examples, 
which becomes critical at longer sequence lengths, as memory constraints limit batching across examples.


