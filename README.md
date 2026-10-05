\# SentimentScope



SentimentScope is a transformer-based binary sentiment classification project built using the IMDB movie review dataset.



\## Project Overview



The goal of this project is to classify movie reviews as either \*\*Positive\*\* or \*\*Negative\*\* using a custom Transformer architecture.



The project uses the `bert-base-uncased` tokenizer for subword tokenization and a custom GPT-style Transformer model implemented in PyTorch.



\## Dataset



The project uses the IMDB Large Movie Review Dataset.



\- Training reviews: 25,000

\- Testing reviews: 25,000

\- Classes: Positive and Negative

\- Training split: 22,500 reviews

\- Validation split: 2,500 reviews



The original IMDB dataset is not included in this repository.



Dataset source: Stanford AI Lab  

https://ai.stanford.edu/\~amaas/data/sentiment/



\## Model Architecture



The model contains:



\- Token embedding layer

\- Positional embedding layer

\- Multi-head self-attention

\- Feed-forward networks

\- Layer normalization

\- Residual connections

\- Mean pooling

\- Binary classification head



The classification head produces two logits:



\- Class 0: Negative

\- Class 1: Positive



\## Training



Training was performed using PyTorch on CPU.



Configuration:



\- Epochs: 3

\- Batch size: 16

\- Maximum sequence length: 128

\- Optimizer: AdamW

\- Learning rate: 0.0003

\- Loss function: CrossEntropyLoss

\- Embedding dimension: 128

\- Transformer layers: 4

\- Attention heads: 4



\## Results



| Metric | Result |

|---|---:|

| Final Validation Accuracy | 80.92% |

| Final Test Accuracy | 77.02% |

| Final Test Loss | 0.4829 |



The model achieved more than the required 75% test accuracy.



\## Example Predictions



\### Positive Review



> This movie was absolutely fantastic. The story was engaging and the performances were excellent.



Prediction: \*\*Positive\*\*



Confidence: \*\*95.86%\*\*



\### Negative Review



> This movie was terrible. The story was boring, the acting was poor, and I did not enjoy watching it.



Prediction: \*\*Negative\*\*



Confidence: \*\*99.98%\*\*



\## Repository Contents



\- `SentimentScope.ipynb` — Complete project notebook

\- `sentimentscope\_model.pt` — Trained model checkpoint

\- `requirements.txt` — Python dependencies

\- `.gitignore` — Files excluded from Git

\- `aclImdb/` — Dataset directory, not included in GitHub

\- `aclImdb\_v1.tar.gz` — Original dataset archive, not included in GitHub



\## How to Run



1\. Clone the repository.



2\. Install the required Python packages:



```bash

pip install -r requirements.txt

