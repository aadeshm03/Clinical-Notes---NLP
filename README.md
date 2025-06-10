# Clinical Notes NLP Classifier

This project uses Natural Language Processing (NLP) to classify clinical notes into diagnostic labels using a fine-tuned transformer model. It leverages pre-trained biomedical models such as ClinicalBERT and Clinical ModernBERT to identify conditions based on unstructured clinical text.

## 🧠 Project Overview

Given a dataset of clinical notes along with patient summaries, an individual note and paired diagnosis label were extracted. The model learns to predict the correct condition based on the text. Example conditions include:
- Idiopathic osteonecrosis of the femoral head  
- Bone marrow edema  
- Osteomalacia  
- Diaphragmatic defect  
- Drug-induced dystonia (user-supplied note)

## 🔍 Dataset Structure
Each row in the dataset includes:
- `text`: A clinical note or case description  
- `label`: The diagnosis/condition  
"A 36-year-old female presented with...", "idiopathic osteonecrosis of the femoral head"
"A 49-year-old male with elbow pain...", "proximal ulnar shaft fracture"

## 🧪 Model Architecture
The model is based on ehbio/clinical-modern-bert-base-uncased, a transformer pretrained on biomedical and clinical text. Fine-tuning was done using HuggingFace's transformers library with a custom classification head.
Features
- Long input support (up to 8,192 tokens)
- Trained on real-world EMR notes (e.g., MIMIC-IV)
