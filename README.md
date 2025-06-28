# 🧠 Fine-Tuning LLMs for Text Classification + Gradio

This repository is part of my personal hands-on practice in fine-tuning **large language models (LLMs)** for classification tasks. It includes implementations and experiments with multiple training strategies on encoder-based models.

> ✅ We focus on **encoder-based models** (also called **representation models**) like BERT, RoBERTa, and SentenceTransformers. These models convert input text into dense vector embeddings optimized for classification and other downstream tasks.

> 📚 This project is based on the **_Hands-On Large Language Models_** book and serves as my practical exploration of fine-tuning techniques for real-world problems.

## 🔧 Methods Practiced

| Method                     | Description                                                                                   | Pros                                   | Cons                                |
|----------------------------|-----------------------------------------------------------------------------------------------|----------------------------------------|-------------------------------------|
| **Full Fine-Tuning (Supervised)** | Train all parameters of the pre-trained LLM on a labeled dataset                               | Highest accuracy when data is sufficient | Very compute-heavy and slow         |
| **Freezing Layers**         | Freeze lower layers and fine-tune only top layers (e.g., classification head or top transformer blocks) | Reduces compute and overfitting         | May limit performance               |
| **SetFit**                  | Contrastive learning on sentence embeddings (no tokenization), then a classifier trained on embeddings | Extremely fast, no need for GPUs        | Limited to sentence-level tasks     |
| **MLM (Masked Language Modeling)** | Self-supervised pretraining task where random tokens are masked and predicted                  | Helps domain adaptation or unsupervised learning | Not directly suited for classification (requires task-specific head later) |

## 📌 Summary

- ✅ Practicing **full fine-tuning**, **layer freezing**, **SetFit**, and **MLM-based pretraining**.
- Use **Full Fine-Tuning** for large datasets and high-performance needs.  
- **Freezing Layers** is a compromise between performance and efficiency.  
- **SetFit** is ideal for quick, lightweight training with small data.  
- **MLM** is useful for domain-specific pretraining before classification.
