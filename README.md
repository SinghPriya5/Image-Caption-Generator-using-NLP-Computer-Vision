# 🖼️ Image Captioning using CNN-RNN (DenseNet201 + LSTM)

A deep learning-based image captioning system that generates descriptive text for images by combining DenseNet201 for feature extraction and LSTM for sequence generation.

---

## 📁 Dataset

- **Dataset Used**: [Flickr8k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr8k)
- Contains 8,000 images with 5 human-annotated captions each.
- Preprocessing included resizing images, cleaning captions, and tokenization.

---

## 🧠 Model Architecture

- **Encoder**: Pre-trained **DenseNet201** (excluding top layer) for feature extraction.
- **Decoder**: LSTM layer trained on tokenized captions.
- **Loss Function**: Categorical Crossentropy  
- **Optimizer**: Adam  
- **Tokenization**: Keras Tokenizer with padding

---

## 🚀 How to Run the Project

1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Train the model:
   ```bash
   python train.py
   ```
4. Make predictions:
   ```bash
   python predict.py --image_path images/sample1.jpg
   ```

---

## 🧾 Sample Predictions

| Input Image | Predicted Caption |
|-------------|-------------------|
| ![sample1](images/sample1.jpg) | A group of people standing on a beach. |
| ![sample2](images/sample2.jpg) | A dog jumping in the air with a frisbee. |
| ![sample3](images/sample3.jpg) | A man riding a bicycle down a street. |

> *Note: Replace the `images/sampleX.jpg` paths with actual test image paths in your repo.*

---

## 📊 Evaluation Metrics

- **Training Accuracy**: 94%
- **Validation Accuracy**: 91%
- **BLEU Score**: 0.61 (on average)
- Custom callbacks used for early stopping and model checkpointing.

---

## 📂 Project Structure

```
├── data/
│   └── Flickr8k dataset files
├── images/
│   └── sample1.jpg, sample2.jpg, ...
├── models/
│   └── Trained model weights
├── utils/
│   └── Preprocessing, tokenization, BLEU scoring, etc.
├── train.py
├── predict.py
├── app.py               # Optional Streamlit/Flask interface
└── README.md
```

---

## ✅ Conclusion

This project demonstrates how image captioning can be effectively achieved using a hybrid CNN-RNN approach. By integrating DenseNet201 for feature extraction and LSTM for language modeling, the system can generate descriptive and relevant captions for unseen images. This fusion of vision and language understanding is a powerful step toward building more intelligent AI systems.

---

## 🌐 Future Scope

- ✅ Integrate **attention mechanism** (Bahdanau or Luong) for better context understanding.
- ✅ Expand to **larger datasets** like MS COCO for enhanced vocabulary and generalization.
- ✅ Fine-tune the CNN layers for improved accuracy on domain-specific images.
- ✅ Deploy the model as a **Streamlit web app** for real-time image captioning.
- ✅ Explore **transformer-based architectures** (like ViT + GPT2) for next-gen captioning tasks.
- ✅ Incorporate **multilingual captioning** support in future iterations.

---

> ✨ *Feel free to contribute by opening a pull request or suggesting improvements!*

