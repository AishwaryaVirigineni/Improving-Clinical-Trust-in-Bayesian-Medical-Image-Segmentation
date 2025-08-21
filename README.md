# Improving Clinical Trust in Bayesian Medical Image Segmentation  

This project explores **Bayesian U-Net** architectures for lung segmentation in chest X-rays with an emphasis on **uncertainty-aware learning**. By aligning predictive uncertainty with segmentation errors, the model improves both **accuracy** and **clinical trustworthiness**.  

---

## 📌 Overview
- **Problem:** Conventional U-Nets lack reliable uncertainty estimation, risking overconfident errors in clinical use.  
- **Approach:**  
  - Bayesian U-Net with **Monte Carlo dropout** for epistemic uncertainty.  
  - **Aleatoric uncertainty simulation** using random mask perturbations.  
  - Introduced an **Accuracy vs. Uncertainty (AvU) loss** to penalize miscalibrated confidence.  
- **Dataset:** Montgomery County Chest X-ray Database.  

---

## ⚙️ Methods
- Compared **3 models**:  
  1. Standard U-Net  
  2. Bayesian U-Net  
  3. Bayesian U-Net + AvU loss  
- Training details:  
  - Input: 256×256 grayscale lung X-rays  
  - Optimizer: Adam (lr=1e-3)  
  - Dropout: 0.3  
  - Monte Carlo samples: 10  

---

## 📊 Results
- **Bayesian U-Net** achieved the highest Dice score (0.922).  
- **Bayesian U-Net + AvU** improved uncertainty-error alignment (AvU score: 0.077), making uncertainty maps more clinically meaningful.  
- Visualizations show higher uncertainty around lung boundaries—where errors are most likely.  

---

## 🚀 Usage
Simply open and run the provided Jupyter Notebook in this repository:  
```bash
jupyter notebook Bayesian_Unet_LungSegmentation.ipynb
```

Dependencies:  
- PyTorch  
- NumPy  
- Matplotlib  
- scikit-image  

---

## 👥 Team
- Aishwarya Virigineni  
- Kanisha Raja  
- Nithya Kaandru  

