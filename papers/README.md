# Research Publications

Ten projects across machine learning, NLP, computer vision, cybersecurity, and systems — each with a dedicated IEEE conference paper (LaTeX source in this directory) and implementation in its own repository.

---

## Papers with published PDFs

| # | Title | Repo | Paper |
|---|-------|------|-------|
| 1 | [WarLens: Transfer Learning for Event Classification in Conflict Zones](#1-warlens) | [warlens](https://github.com/omprxkash/warlens) | [PDF](https://github.com/omprxkash/warlens/blob/main/docs/paper/WarLens%20%E2%80%93%20Transfer%20Learning%20for%20Event%20Classification%20in%20Conflict%20Zones.pdf) · [.tex](https://github.com/omprxkash/warlens/blob/main/docs/paper/conference_101719.tex) |
| 2 | [LLM-Augmented OCR for Robust Document Understanding](#2-llm-aided-ocr) | [llm-aided-ocr](https://github.com/omprxkash/llm-aided-ocr) | [PDF](https://github.com/omprxkash/llm-aided-ocr/blob/main/docs/research/21BCE1950_53074.pdf) · [Patent](https://github.com/omprxkash/llm-aided-ocr/blob/main/docs/patents/PATENT_OCR_LLM_17_mar.docx) |
| 3 | [GemVAE: Graph-Enhanced Multi-Modal VAE for Image Classification](#3-gemvae--graph-attention) | [graph-attention-vision-transformers](https://github.com/omprxkash/graph-attention-vision-transformers) | [PDF](https://github.com/omprxkash/graph-attention-vision-transformers/blob/master/paper/GemVAE_Pugazhendhi_2023.pdf) · [.tex](https://github.com/omprxkash/graph-attention-vision-transformers/blob/master/paper/GemVAE_paper.tex) |
| 4 | [Intrusion Detection Using ML and Neural Network Approaches](#4-intrusion-detection) | [intrusion-detection-system-cyber](https://github.com/omprxkash/intrusion-detection-system-cyber) | [PDF](https://github.com/omprxkash/intrusion-detection-system-cyber/blob/main/INTRUSION_DETECTION_IN_A_NETWORK_USING_MACHINE_LEARNING_AND_NEURAL_NETWORK%5B1%5D.pdf) |
| 5 | [Multi-Disease Prediction Using Ensemble Machine Learning](#5-disease-prediction) | [disease-prediction-ml](https://github.com/omprxkash/disease-prediction-ml) | [PDF](https://github.com/omprxkash/disease-prediction-ml/blob/main/21BCE1950_21BCE5828_DA3_afterreview.pdf) |
| 6 | [BERT-Based Named Entity Recognition for Domain-Specific IE](#6-named-entity-recognition) | [named-entity-recognition-nlp](https://github.com/omprxkash/named-entity-recognition-nlp) | [PDF](https://github.com/omprxkash/named-entity-recognition-nlp/blob/main/ResearchPaper_bert.pdf) |
| 7 | [Histopathological Cancer Detection via Patch-Based CNN](#7-cancer-detection) | [histopathological-cancer-detection](https://github.com/omprxkash/histopathological-cancer-detection) | [PDF](https://github.com/omprxkash/histopathological-cancer-detection/blob/main/cancer%20research%20paper.pdf) |
| 8 | [Neural Texture Stylization Using Deep Feature Representations](#8-texture-stylization) | [texture-model-stylization](https://github.com/omprxkash/texture-model-stylization) | [PDF](https://github.com/omprxkash/texture-model-stylization/blob/master/Neural_Texture_Stylization_Omprakash_2025.pdf) |
| 9 | [Cross-Lingual Transfer for Low-Resource NLP](#9-multilingual-nlp) | [multilingual-resource-models](https://github.com/omprxkash/multilingual-resource-models) | [.tex](https://github.com/omprxkash/multilingual-resource-models/blob/master/paper/main.tex) |
| 10 | [AI-Integrated Smart Blood Bank Platform](#10-blood-bank) | [blood-bank-platform](https://github.com/omprxkash/blood-bank-platform) | [paper.tex](blood-bank/paper.tex) ← draft |

---

## 1. WarLens

**Transfer Learning for Event Classification in Conflict Zones**

Applied transfer learning (VGG-16, ResNet-50, EfficientNet) to satellite and open-source imagery from active conflict zones to classify events — airstrikes, ground movement, infrastructure damage. Trained on a curated multi-source dataset with domain adaptation to handle the distribution gap between civilian image datasets and conflict-zone imagery.

- **Repo**: [warlens](https://github.com/omprxkash/warlens)
- **Paper PDF**: [WarLens – Transfer Learning for Event Classification in Conflict Zones.pdf](https://github.com/omprxkash/warlens/blob/main/docs/paper/WarLens%20%E2%80%93%20Transfer%20Learning%20for%20Event%20Classification%20in%20Conflict%20Zones.pdf)
- **LaTeX source**: [conference_101719.tex](https://github.com/omprxkash/warlens/blob/main/docs/paper/conference_101719.tex)
- **Project report**: [52227_21BCE1950.pdf](https://github.com/omprxkash/warlens/blob/main/docs/report/52227_21BCE1950.pdf)
- **IEEE template**: [warlens/paper.tex](warlens/paper.tex)

---

## 2. LLM-Aided OCR

**LLM-Augmented OCR for Robust Document Understanding**

Built a two-stage pipeline that combines traditional OCR (Tesseract, PaddleOCR) with a large language model post-processing layer to correct extraction errors, understand document layout semantics, and answer questions over scanned documents. Filed a patent for the LLM-OCR integration architecture.

- **Repo**: [llm-aided-ocr](https://github.com/omprxkash/llm-aided-ocr)
- **Research paper**: [21BCE1950_53074.pdf](https://github.com/omprxkash/llm-aided-ocr/blob/main/docs/research/21BCE1950_53074.pdf)
- **Patent filing**: [PATENT_OCR_LLM_17_mar.docx](https://github.com/omprxkash/llm-aided-ocr/blob/main/docs/patents/PATENT_OCR_LLM_17_mar.docx)
- **Capstone presentation**: [capstone_ppt.pptx](https://github.com/omprxkash/llm-aided-ocr/blob/main/docs/presentations/capstone_ppt.pptx)
- **IEEE template**: [llm-aided-ocr/paper.tex](llm-aided-ocr/paper.tex)

---

## 3. GemVAE / Graph Attention

**GemVAE: Graph-Enhanced Multi-Modal Variational Autoencoder**

A hybrid architecture combining sparse k-NN patch graphs with Gaussian edge weights (GAT) and an EfficientNetV2-S vision backbone, fused through a variational autoencoder for CIFAR-100 classification. Four model variants benchmarked: baseline ViT, GAT-only, GemVAE, GemVAE+contrastive.

- **Repo**: [graph-attention-vision-transformers](https://github.com/omprxkash/graph-attention-vision-transformers)
- **Paper PDF**: [GemVAE_Pugazhendhi_2023.pdf](https://github.com/omprxkash/graph-attention-vision-transformers/blob/master/paper/GemVAE_Pugazhendhi_2023.pdf)
- **LaTeX source**: [GemVAE_paper.tex](https://github.com/omprxkash/graph-attention-vision-transformers/blob/master/paper/GemVAE_paper.tex)
- **References**: [references.bib](https://github.com/omprxkash/graph-attention-vision-transformers/blob/master/paper/references.bib)
- **IEEE template**: [gemvae-graph-attention/paper.tex](gemvae-graph-attention/paper.tex)

---

## 4. Intrusion Detection

**Intrusion Detection in a Network Using ML and Neural Networks**

Compared supervised ML classifiers (Random Forest, SVM, XGBoost) and neural network architectures (MLP, LSTM) on KDD Cup 99 and NSL-KDD datasets for network intrusion detection. Identified feature importance patterns and evaluated detection rate vs. false positive tradeoffs across attack categories.

- **Repo**: [intrusion-detection-system-cyber](https://github.com/omprxkash/intrusion-detection-system-cyber)
- **Paper PDF**: [INTRUSION_DETECTION...pdf](https://github.com/omprxkash/intrusion-detection-system-cyber/blob/main/INTRUSION_DETECTION_IN_A_NETWORK_USING_MACHINE_LEARNING_AND_NEURAL_NETWORK%5B1%5D.pdf)
- **Presentation**: [.pptx](https://github.com/omprxkash/intrusion-detection-system-cyber/blob/main/Intrusion-Detection-in-a-Network-using-Machine-Learning-and-Neural-Network-Approaches.pptx)
- **IEEE template**: [intrusion-detection/paper.tex](intrusion-detection/paper.tex)

---

## 5. Disease Prediction

**Multi-Disease Prediction Using Ensemble Machine Learning on Clinical Records**

Built an ensemble (Random Forest + Gradient Boosting + Logistic Regression) on clinical health record datasets to predict multiple diseases simultaneously. Addressed class imbalance with SMOTE, used SHAP for model explainability, and benchmarked against standalone classifiers on accuracy, precision, and AUC-ROC.

- **Repo**: [disease-prediction-ml](https://github.com/omprxkash/disease-prediction-ml)
- **Research report**: [21BCE1950_21BCE5828_DA3_afterreview.pdf](https://github.com/omprxkash/disease-prediction-ml/blob/main/21BCE1950_21BCE5828_DA3_afterreview.pdf)
- **Notebook**: [21BCE1950_21BCE5828_code.ipynb](https://github.com/omprxkash/disease-prediction-ml/blob/main/21BCE1950_21BCE5828_code.ipynb)
- **IEEE template**: [disease-prediction/paper.tex](disease-prediction/paper.tex)

---

## 6. Named Entity Recognition

**BERT-Based Named Entity Recognition for Domain-Specific Information Extraction**

Fine-tuned BERT and compared with spaCy custom NER and BiLSTM-CRF on a domain-specific NER dataset. Evaluated entity-level F1 across PER, ORG, LOC, and MISC categories, with a focus on low-resource adaptation using limited annotated data.

- **Repo**: [named-entity-recognition-nlp](https://github.com/omprxkash/named-entity-recognition-nlp)
- **Research paper**: [ResearchPaper_bert.pdf](https://github.com/omprxkash/named-entity-recognition-nlp/blob/main/ResearchPaper_bert.pdf)
- **Survey**: [21BCE1950_5828_NLP_DA1SURVEY.pdf](https://github.com/omprxkash/named-entity-recognition-nlp/blob/main/21BCE1950_5828_NLP_DA1SURVEY.pdf)
- **Notebook**: [BERT_NAMED_ENTITY_RECOGNITION.ipynb](https://github.com/omprxkash/named-entity-recognition-nlp/blob/main/BERT_NAMED_ENTITY_RECOGNITION.ipynb)
- **IEEE template**: [named-entity-recognition/paper.tex](named-entity-recognition/paper.tex)

---

## 7. Cancer Detection

**Histopathological Cancer Detection via Patch-Based CNN and Transfer Learning**

Developed a patch-level CNN pipeline for binary cancer detection in histopathological slide images. Used TensorFlow with GPU-accelerated training, data augmentation, and patch-level inference aggregated to slide-level predictions. Compared VGG-16, ResNet-50, and InceptionV3 backbones.

- **Repo**: [histopathological-cancer-detection](https://github.com/omprxkash/histopathological-cancer-detection)
- **Research paper**: [cancer research paper.pdf](https://github.com/omprxkash/histopathological-cancer-detection/blob/main/cancer%20research%20paper.pdf)
- **Presentation**: [ppt.pdf](https://github.com/omprxkash/histopathological-cancer-detection/blob/main/ppt.pdf)
- **IEEE template**: [cancer-detection/paper.tex](cancer-detection/paper.tex)

---

## 8. Texture Stylization

**Neural Texture Stylization Using Deep Feature Representations**

Implemented neural style transfer and texture synthesis using VGG-19 feature maps. Extended Gatys et al.'s gram matrix formulation with multi-scale texture loss and content-adaptive style blending. Evaluated perceptual quality on a benchmark set of artistic styles and natural textures.

- **Repo**: [texture-model-stylization](https://github.com/omprxkash/texture-model-stylization)
- **Paper PDF**: [Neural_Texture_Stylization_Omprakash_2025.pdf](https://github.com/omprxkash/texture-model-stylization/blob/master/Neural_Texture_Stylization_Omprakash_2025.pdf)
- **IEEE template**: [texture-stylization/paper.tex](texture-stylization/paper.tex)

---

## 9. Multilingual NLP

**Cross-Lingual Transfer for Low-Resource NLP**

Fine-tuned mBERT and XLM-RoBERTa on high-resource languages and evaluated zero-shot and few-shot transfer to low-resource language pairs. Compared adapter-based fine-tuning against full fine-tuning on NER and text classification tasks. LaTeX source and bib file in the repo.

- **Repo**: [multilingual-resource-models](https://github.com/omprxkash/multilingual-resource-models)
- **LaTeX source**: [paper/main.tex](https://github.com/omprxkash/multilingual-resource-models/blob/master/paper/main.tex)
- **References**: [paper/references.bib](https://github.com/omprxkash/multilingual-resource-models/blob/master/paper/references.bib)
- **IEEE template**: [multilingual-nlp/paper.tex](multilingual-nlp/paper.tex)

---

## 10. Blood Bank

**AI-Integrated Smart Blood Bank Platform for Real-Time Donor-Recipient Matching**

A full-stack PHP + MySQL blood bank system with donor registration, blood type inventory management, hospital request routing, and urgency-based matching. This subfolder contains an IEEE conference paper draft for the AI-driven matching component — work in progress.

- **Repo**: [blood-bank-platform](https://github.com/omprxkash/blood-bank-platform)
- **IEEE template**: [blood-bank/paper.tex](blood-bank/paper.tex) ← **draft, fill in your results**

---

## How to compile any .tex file

```bash
# Using pdflatex (local)
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex

# Using Overleaf
# Upload paper.tex → Project → Compile
# Template: IEEE Conference (IEEEtran)
```

All templates use `\documentclass[conference]{IEEEtran}` and compile cleanly on Overleaf with no additional packages beyond the standard IEEE set.
