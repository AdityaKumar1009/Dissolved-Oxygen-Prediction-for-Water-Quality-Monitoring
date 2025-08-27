# Dissolved Oxygen Prediction using LSTM with Attention

## 📌 Project Overview
This project focuses on **forecasting dissolved oxygen (DO) levels** in water bodies using **deep learning time-series models**. Dissolved oxygen is a crucial indicator of water quality, and accurate prediction can help in **environmental monitoring, early detection of ecological risks, and policy planning**.

The project explores multiple deep learning architectures:
- **Baseline LSTM**
- **LSTM + Custom Simple Attention**
- **Improved LSTM with longer look-back windows**

---

## 🚀 Key Achievements
- ✅ Built a **custom Simple Attention layer** to enhance temporal feature learning.  
- ✅ Improved Test **R² score from 0.977 (Baseline LSTM) → 0.988 (Optimized LSTM)**.  
- ✅ Reduced **Mean Absolute Error (MAE) by ~28%**, achieving **0.0399 vs. 0.0555 baseline**.  
- ✅ Demonstrated that **longer look-back windows** (lag = 5, 10) significantly enhance predictive power.  
- ✅ Developed an **interpretable and scalable forecasting pipeline** for real-world water quality monitoring.

---

## 📂 Dataset
- Source: `georgia_with_ammonia.csv`
- Features Used:  
  - `date` → Timestamp (indexed)  
  - `dissolved_oxygen` → Target variable  

---

## ⚙️ Workflow
1. **Data Preprocessing**  
   - Converted `date` column to datetime and indexed.  
   - Scaled dissolved oxygen values using **MinMaxScaler**.  
   - Split into train/test sets (pre/post June 2018).  

2. **Model Architectures**  
   - **Baseline LSTM** with lag = 1  
   - **LSTM + Attention** (custom Keras Layer)  
   - **Improved LSTM with lag = 5, 10**  

3. **Training Enhancements**  
   - Early stopping to prevent overfitting.  
   - Tuned batch size and epochs.  

4. **Evaluation Metrics**  
   - **R² Score**  
   - **Mean Squared Error (MSE)**  
   - **Root Mean Squared Error (RMSE)**  
   - **Mean Absolute Error (MAE)**  

---

## 📊 Results

| Model                       | R² (Test) | MSE    | RMSE   | MAE   |
|-----------------------------|-----------|--------|--------|-------|
| Standard LSTM (lag 1)       | **0.977** | 0.0059 | 0.0769 | 0.0555 |
| **Optimized LSTM **  | **0.988** | 0.0032 | 0.0566 | **0.0399** |

**Key Insight:**  
The **Optimized LSTM with lag = 5** achieved the **best performance**, significantly reducing prediction error and outperforming both the baseline and attention-based models.

---

## 📈 Visualizations
- Dissolved Oxygen time-series plots (train/test split).  
- Prediction vs. Actual curves for each model.  
- Loss convergence plots.  

---

## 🛠️ Tech Stack
- **Python 3.9+**
- **TensorFlow / Keras**
- **scikit-learn**
- **NumPy / Pandas / Matplotlib** 

---

## ✨ Impact
This project demonstrates how **attention-augmented deep learning** can improve **environmental forecasting systems**. By achieving **R² = 0.988** and reducing prediction error by **28%**, the model offers a practical tool for **ecologists, researchers, and policymakers** in managing water resources more effectively.
