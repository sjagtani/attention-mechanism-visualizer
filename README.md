# Attention Mechanism Visualizer

This repository provides tools for visualizing the attention mechanism that powers modern transformer models like GPT and BERT. The implementation is based on concepts from Andrej Karpathy's "Neural Networks: Zero to Hero" course.

## What is Attention?

Attention is a mechanism that allows a model to focus on different parts of the input sequence when producing each element of the output. It's one of the key innovations that led to the transformer architecture and the current generation of large language models.

## Features

This project offers a clean, from-scratch implementation of self-attention, allowing for transparent examination of the mechanism's inner workings. It provides comprehensive visualization tools that show exactly how attention heads focus on different parts of input sequences.

The implementation explores various attention patterns including standard self-attention, causal attention (as used in decoder-only models like GPT), local attention (which improves efficiency for long sequences), and global-local attention (a hybrid approach combining global context with local focus). 

The project also demonstrates the effects of positional encoding, showing how it fundamentally changes attention behavior.

## Getting Started

### Prerequisites

```bash
pip install -r requirements.txt
```

### Running the Visualizer

You can either:
1. Run the Python script:

```bash
python attention_mechanism_visualizer.py
```

2. Open and run the Jupyter notebook:

```bash
jupyter notebook attention_mechanism_visualizer.ipynb
```

Or open the notebook in Google Colab! [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1GABDhxtLyIVrMDTnpzGegXsaWS6MYvmb#scrollTo=S6iKcdVI4TAi)

## Implementation Details

The implementation includes a `SelfAttention` class that builds multi-head attention from scratch, following the principles outlined in the original transformer paper. It provides functions to generate token embeddings (simplified for demonstration purposes) and comprehensive visualization tools for displaying attention weights in an intuitive manner.

The code implements various attention masking patterns to demonstrate different attention mechanisms used in modern transformer architectures. Additionally, it includes a simple positional encoding system based on sine/cosine functions, allowing for exploration of how position information influences attention behavior.

## Extending the Code

This implementation provides several opportunities for extension and further exploration.

You could enhance the model by adding layer normalization and feed-forward networks to create a complete transformer layer implementation. For those interested in encoder-decoder architectures, implementing cross-attention would be a valuable addition. The positional encoding system could be extended with more complex schemes to explore their effects on model behavior. 

An especially interesting extension would be integrating with pre-trained models like BERT or GPT to visualize how attention operates in state-of-the-art language models that have learned from vast amounts of data.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## References

* [Attention Is All You Need](https://arxiv.org/abs/1706.03762) - Original transformer paper
* [Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html) - Andrej Karpathy's course
* [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) - Jay Alammar's visualization guide

## Acknowledgments

* Inspired by Andrej Karpathy's "Neural Networks: Zero to Hero" course
* Based on the concepts from "Attention Is All You Need" paper
