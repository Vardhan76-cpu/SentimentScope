\# SentimentScope



\*\*SentimentScope\*\* is a transformer-based sentiment analysis system designed to classify movie reviews as \*\*Positive\*\* or \*\*Negative\*\*.



The project explores how Transformer architectures can be adapted for text classification using the \*\*IMDB Large Movie Review Dataset\*\*. It combines subword tokenization, a custom GPT-style Transformer implemented in PyTorch, supervised training, validation, and final test evaluation.



\---



\## Overview



SentimentScope takes a raw movie review as input and predicts its sentiment using a two-class classification model.



The complete workflow includes:



\- IMDB dataset preparation

\- Exploratory data analysis

\- Train/validation splitting

\- Subword tokenization using `bert-base-uncased`

\- Custom PyTorch Dataset and DataLoader

\- Transformer-based feature extraction

\- Binary sentiment classification

\- Training and validation

\- Final evaluation on the untouched test dataset

\- Single-review inference



The model produces two output logits corresponding to:



\- \*\*Class 0 → Negative\*\*

\- \*\*Class 1 → Positive\*\*



\---



\## Dataset



The project uses the \*\*IMDB Large Movie Review Dataset\*\*, containing 50,000 labelled movie reviews.



| Dataset | Reviews |

|---|---:|

| Training set | 25,000 |

| Validation set | 2,500 |

| Training subset | 22,500 |

| Test set | 25,000 |

| Classes | 2 |



The original dataset is intentionally excluded from this repository because of its size.



\### Dataset Source



The IMDB dataset can be obtained from the Stanford AI Lab dataset directory:



https://ai.stanford.edu/\~amaas/data/



The expected archive is:



```text

aclImdb\_v1.tar.gz

