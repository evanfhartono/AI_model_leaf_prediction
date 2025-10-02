# 🌿 Leaf Classification with CNN + FastAPI

This project implements a **Convolutional Neural Network (CNN)** model to classify **11 plant species** based on their leaf images.  
The system is deployed with **FastAPI backend** and a simple **HTML interface**, allowing users to upload an image and get predictions in real time.

---

## 📖 Background
Automatic plant identification has significant applications in **ecology, biodiversity monitoring, and botany research**.  
Manual identification is time-consuming and requires expertise, while **machine learning models** can provide fast and accurate predictions.  

This project uses a **CNN-based model** trained on multiple plant leaf datasets to classify leaves with high accuracy.  

---

## 🎯 Objectives
- Automate **leaf species identification** using CNN.
- Build a **web prototype** with FastAPI + HTML interface.
- Provide **real-time classification** with confidence scores.
- Demonstrate an **AI application** that bridges model + user-friendly interface.

---

## 🛠️ Tech Stack
- **Python, TensorFlow/Keras** – Model training
- **FastAPI** – Backend server
- **HTML + JavaScript** – User interface
- **Docker (optional)** – Containerized deployment
- **Kaggle Dataset** – Leaf images (Lemon, Mango, Pomegranate, Basil, Pongamia, Jamun, Alstonia Scholaris, Arjun, Chinar, Guava, Jatropha)

---

## 📂 Project Structure
```
AI_model_leaf_prediction/
│
├── api/ # FastAPI backend
│ ├── main.py # Main server
│ ├── requirements.txt # Python dependencies
│ └── model/ # Saved CNN model
│
├── frontend/ # HTML + JS interface
│ └── index.html
│
└── README.md
```


---

## 📊 Model Architecture
- Input: 256x256 leaf images
- Conv Layers: 4 convolution layers (3x3 filters, ReLU, max-pooling)
- Dense Layer: 64 units (ReLU)
- Output Layer: 11 units (Softmax for 11 plant classes)
- Optimizer: Adam
- Loss: SparseCategoricalCrossentropy
- Data Augmentation + Normalization applied

**Performance:**
- Training Accuracy: **92.48%**
- Validation Loss: **0.20**
- Example predictions: Mango leaf (99.9%), Jamun leaf (97.3%), Pomegranate leaf (99.99%) :contentReference[oaicite:1]{index=1}

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/evanfhartono/AI_model_leaf_prediction.git
cd AI_model_leaf_prediction
```

### 2. Install dependencies
```
pip install -r api/requirements.txt
```

### 3. Run the FastAPI backend
```
cd api
python main.py
```

Wait until the server starts (default port: 8000 or as configured).

### 4. Run the frontend

Open frontend/index.html with Live Server (VS Code extension) or any static server.

Make sure the port configuration in main.py matches your HTML server port:
```
origins = [
    "http://127.0.0.1:5501", 
    "http://localhost:5501",
    "http://127.0.0.1:[Your HTML Live Server Port]"
]
```

5. Use the Prototype

Upload a leaf image (you can use samples from Kaggle Dataset).
Click Classify.
Get prediction + confidence score.

### Upload & Classification UI
<img width="1228" height="691" src="https://github.com/user-attachments/assets/32b70911-296e-4102-8400-60c2d16b2f9d" /> 

### Plot preivew
<img width="1228" height="691" src="https://github.com/user-attachments/assets/fe18be20-4de4-448d-85a2-db031cb4a904" /> 
<img width="1231" height="689" src="https://github.com/user-attachments/assets/ff6db7a7-5407-4b28-a85d-b1e2a3007e0b" />
<img width="1228" height="691" alt="chrome_2zDB3v6E7H" src="https://github.com/user-attachments/assets/9a71b148-727f-4ce0-b3cf-1e6b70e9a81d" />
<img width="442" height="348" src="https://github.com/user-attachments/assets/e6521e2b-35b6-4684-a119-a2e9d08de77b" />

### 🔮 Future Work

Add more plant species to dataset.

Improve generalization for different lighting/backgrounds.

Build a mobile-friendly app version.

Explore Transformers / EfficientNet for higher accuracy.

---

### 📚 References

Chakravarthy, K. S. (2024). Plant Species Identification Using CNN. IJISAE.

Taslim, A. et al. (2021). Plant leaf identification using CNN. BEEI Journal.

Azlah, M.A.F. et al. (2019). Review on Techniques for Plant Leaf Classification. Computers.


