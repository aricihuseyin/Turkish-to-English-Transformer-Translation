Turkish-to-English Translation using Transformer Model

Overview

This project implements a Turkish-to-English translation model using the Transformer architecture. The goal is to train the model on a dataset of Turkish-English sentence pairs, evaluate its performance, and demonstrate its translation capabilities. This work is based on techniques commonly used in the literature for sequence-to-sequence tasks with Transformers.

Dataset
The dataset used for this project contains 555,190 Turkish-English sentence pairs. For the purposes of this project:

30% of the data is used for training (166,557 sentences).
70% of the data is used for testing (388,633 sentences).
Data Preparation
Tokenization: Sentences are tokenized into words/tokens.
Padding: Sequences are padded to ensure uniform length.
Vocabulary Building: A dictionary mapping words to indices is created.
Model Architecture
The Transformer model consists of an encoder and a decoder, both of which include several layers of Multi-Head Attention and Feed Forward Neural Networks.

Encoder
Multi-Head Attention: Focuses on different parts of the input sequence simultaneously.
Feed Forward Neural Network: Applies non-linear transformations to each position.
Layer Normalization: Stabilizes and accelerates training.
Positional Encoding: Adds positional information to embeddings.
Decoder
Masked Multi-Head Attention: Prevents attending to future positions in the sequence.
Multi-Head Attention: Integrates encoder outputs to generate context-aware outputs.
Feed Forward Neural Network: Similar to the encoder.
Layer Normalization: Stabilizes and accelerates training.
Positional Encoding: Adds positional information to embeddings.
Embedding
Word Embeddings: Converts words into dense vectors that capture semantic meaning.
Positional Encoding: Adds positional information to embeddings.
Training Process
The model was trained using the following parameters:

Optimizer: Adam with a learning rate of 0.0001.
Loss Function: CrossEntropyLoss with padding index ignored.
Batch Size: 64
Number of Epochs: 5
Max Sequence Length: 16
Training Loop
Teacher Forcing: The actual output is used as the next input during training.
Evaluation Metric: Loss calculated on the test dataset.
Results
Training Loss: The model’s loss decreased over the epochs, indicating successful learning from the training data.
Test Loss: Final test loss was 1.77.
