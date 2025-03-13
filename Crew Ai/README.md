# Sentiment Classification of COVID-19 Tweets Using Transformer Models

## Project Overview
This project focuses on multiclass sentiment classification of COVID-19-related tweets using transformer models. The classification problem involves five sentiment categories:
- Extremely Negative
- Negative
- Neutral
- Positive
- Extremely Positive

Using Hugging Face Trainer, we trained and evaluated different models, testing various hyperparameters to improve performance while considering efficiency limitations.

---

## Dataset & Preprocessing
### Dataset: Corona Virus Tweets

### Preprocessing Steps:
- **Tokenized text** using `AutoTokenizer`:
  - Tokenizer max length: **128**
  - Initially considered 512 tokens but reduced to **128** to optimize memory usage and training speed.
- **Mapped sentiment labels** to numeric values (0-4).
- **Train-test split**: 80:20 while maintaining class distribution across both sets.

---

## Model & Fine-Tuning
### Models Used:
- **DistilBERT**
- **RoBERTa**

### Hyperparameter Testing:

We tested different combinations of dataset sizes, epochs, learning rate, batch size to find the best configuration. Due to efficiency constraints, we conducted hyperparameter tuning across multiple notebooks. 

To find the best configuration, we tested different combinations of:

- **Learning rates**: 0.005, 0.00005
- **Batch sizes**: 8, 16
- **Number of epochs**: 1, 3
- **Weight decay**: 0.01
- **Evaluation strategy**: epoch-based

**Observations:** Lowering the learning rate and increasing the number of epochs resulted in better predictions.

---

## Evaluation & Results
### Metrics Used:
- **Accuracy**

### Observations:
- Different models and parameter settings were tested across multiple notebooks to optimize accuracy.
- Further fine-tuning, additional training time, or more data may improve performance.

---

## Limitations & Challenges
- **Computational Cost**: Training multiple models and tuning hyperparameters required significant resources.
- **Data Size**: A larger dataset could improve generalization and overall performance.

---

## Contributors
**Karolina Motyka**: Responsible for data selection, testing transformer models, fine-tuning the model, testing different hyperparameters, model evaluation, and writing the final documentation.

**Thi Minh Nguyen**: Responsible for dataset selection, testing transformer models, fine-tuning using distilbert, documenting the training process, experimenting with different hyperparameters, evaluating the model, pushing model to fh