# 🛍️ Product Description Generation with BLIP

This project fine-tunes the [BLIP (Bootstrapped Language Image Pretraining)](https://huggingface.co/Salesforce/blip-image-captioning-base) model to generate product descriptions from product images using the [`philschmid/amazon-product-descriptions-vlm`](https://huggingface.co/datasets/philschmid/amazon-product-descriptions-vlm) dataset.

---

## 📌 Project Goals

- Fine-tune a vision-language model (BLIP) to generate descriptive marketing text for products.
- Evaluate generation quality using BERTScore for semantic similarity.

---

## 🗂️ Dataset

- **Name:** [`philschmid/amazon-product-descriptions-vlm`](https://huggingface.co/datasets/philschmid/amazon-product-descriptions-vlm)
- **Samples:** 1,345 Amazon product images with titles and descriptions.
- **Fields:**
  - `image`: Product image
  - `Product Name`: Product title
  - `description`: Marketing-style product description

---

## 🧠 Model

- **Base model:** `Salesforce/blip-image-captioning-base`
- **Architecture:** Vision Transformer + Text Transformer
- **Task:** Conditional image captioning (image → product description)

---

## 🚀 Training Configuration

- `batch_size = 8`
- `epochs = 5`
- `learning_rate = 5e-5`
- `weight_decay = 0.01`
- `fp16 = True` for faster mixed-precision training
- Dataset split: 80% training / 20% testing

---

## 📈 Evaluation

We evaluate the generated descriptions using **[BERTScore](https://arxiv.org/abs/1904.09675)**, which measures semantic similarity between generated and reference texts using BERT embeddings.

| Metric      | Description                            | Result (Test Set) |
|-------------|----------------------------------------|-------------------|
| **BERTScore F1** | Measures meaning-level similarity | **0.8662**        |

> ⚠️ BLEU and ROUGE were not used, as they penalize valid rewordings and are less suited to generative tasks like product description generation.

---

## 🖼️ Sample Output

<img src="assets/sample_image.png" width="600"/>

- **Ground Truth:** Enchant your child with the Cate and Levi 12" Handmade Princess Hand Puppet! Crafted from premium reclaimed wool, each puppet is unique. Colors vary, adding to the charm. Perfect for imaginative play & storytelling. A delightful hand puppet for kids of all ages.
- **Generated:** adorable 3 - piece knitted friends doll set! perfect for imaginative play. soft, huggable, and a collectible addition to any doll collection. shop now!
- **BERTScore F1:** 0.8635

---

## 📝 How to Run

Install dependencies:

```bash
pip install transformers datasets==2.14.6 evaluate bert_score

