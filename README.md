# Vision-Transformers-
Built a plant disease detection system using Vision Transformer (ViT) with PyTorch and Hugging Face. Fine-tuned on the Beans dataset, achieved 95.3% accuracy, added attention visualization, and compared performance with ResNet18 to analyze transformer vs CNN efficiency.

# 🌿 Plant Disease Detection using Vision Transformer (ViT)

This project implements an end-to-end **image classification system** using a **Vision Transformer (ViT)** to detect plant diseases from leaf images. The model is fine-tuned on the Beans dataset to classify leaves into three categories: Angular Leaf Spot, Bean Rust, and Healthy.

🚀 Features
Fine-tuned ViT-Base-Patch16-224 using transfer learning
Complete ML pipeline: preprocessing → training → evaluation
Attention map visualization for interpretability
Performance comparison with ResNet18 (CNN)
Evaluation using accuracy, precision, recall, and F1-score
Reproducible results with saved model artifacts
🛠️ Tech Stack
Python
PyTorch
Hugging Face Transformers & Datasets
scikit-learn
Matplotlib
Jupyter Notebook
📂 Dataset
Beans Dataset (Hugging Face)
Total images: 1295
Classes:
Angular Leaf Spot
Bean Rust
Healthy
Split:
Train: 1034
Validation: 133
Test: 128
⚙️ Methodology
Load dataset using Hugging Face Datasets
Preprocess images (resize, normalization, patching)
Load pre-trained ViT model
Replace classification head for 3 classes
Train using Hugging Face Trainer API
Evaluate using standard metrics
Generate attention maps for interpretability
Compare results with ResNet18
📊 Results
Model	Accuracy	Parameters
ViT	95.3%	86M
ResNet18	97.7%	11M
🔍 Key Insight
Although Vision Transformers achieve high accuracy, ResNet18 outperforms ViT on small datasets, showing that CNNs benefit from inductive bias when data is limited.
🧠 Model Interpretability
The project includes attention map visualization using the CLS token to highlight which regions of the image influenced the model’s prediction.
📸 Sample Output
(Add your images inside a folder named results and update below)
results/
attention_map1.png
attention_map2.png
comparison.png
📦 Project Structure
plant-disease-vit/
├── vision_transformer.ipynb
├── README.md
├── results/
│ ├── attention_maps.png
│ └── comparison.png
└── output.pdf
▶️ How to Run
Clone the repository:
git clone https://github.com/your-username/plant-disease-vit.git
cd plant-disease-vit
Install dependencies:
pip install -r requirements.txt
Run the notebook:
jupyter notebook
🔮 Future Improvements
Train on larger datasets
Use hybrid CNN + Transformer models
Deploy as a web/mobile application
Optimize for real-time predictions
💡 Key Learnings
Vision Transformers vs CNNs
Transfer learning in deep learning
Model interpretability techniques
Real-world ML pipeline development
👩‍💻 Author
Aysha Iram
Artificial Intelligence & Data Science Student
⭐ Acknowledgements
Hugging Face
Google ViT
Makerere AI Lab (Beans Dataset)
