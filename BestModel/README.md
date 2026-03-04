# BestModel – PCL binary classification

**Approach:** RoBERTa-base fine-tuned with **class-weighted cross-entropy** (3 epochs; best checkpoint = epoch 2).  
**Dev F1 (positive class):** 0.5022 (argmax) → **0.5322** with threshold 0.6.  
**Max sequence length:** 256.

## Contents

- **Model (HuggingFace format):** `config.json`, `tokenizer.json`, `tokenizer_config.json` are in this folder. **Weights** (`model.safetensors`, ~475 MB) exceed GitHub’s file size limit and are hosted on Google Drive:  
  **[Download model.safetensors]https://drive.google.com/drive/folders/1D85SUdN6vqlg5Ii_fZFXKRvS3-r5Qgmz?usp=drive_link**  
  Place the downloaded `model.safetensors` in this folder, then load with:  
  `AutoModelForSequenceClassification.from_pretrained("BestModel")`, `AutoTokenizer.from_pretrained("BestModel")`.
- **Code:** `02_training.ipynb` – full training pipeline (data load, tokenize, train baseline + class-weights, threshold tuning, dev.txt / test.txt generation).

## Reproducing dev.txt / test.txt

1. Run the notebook from the repo root (paths use `../data`, `../outputs`).
2. After training, run the threshold-tuning cell (best threshold = 0.6).
3. Run the dev.txt and test.txt cells.  
   Or load this folder and run inference with **threshold = 0.6** on the official dev/test inputs to get the same predictions.
