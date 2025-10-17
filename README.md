
# ✈️ Flight Delay Prediction System

## 🧠 Overview
The **Flight Delay Prediction System** is a deep learning-based project designed to predict **flight arrival delays** using historical data from 2019 to 2023.  
By leveraging multiple neural network architectures — **Feedforward Neural Network (FNN)**, **Simple RNN**, **LSTM**, and **Bidirectional LSTM (BiLSTM)** — the project compares model performance to identify the most accurate approach for delay forecasting.

Dataset Source: [Kaggle – Flight Delay and Cancellation Dataset (2019–2023)](https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023)

---

## 📂 Project Structure
```

Flight-Delay-Prediction-System/
│
├── FNN.ipynb                         # Feedforward Neural Network model
├── RNN_Flight_Delay_Prediction.ipynb # Simple RNN model
├── LSTM_Prediction_Model.ipynb       # LSTM model
├── Bidirectional_LSTM__Model.ipynb   # Bidirectional LSTM model
├── README.md                         # Project documentation
                          

```

---

## ⚙️ Methodology

### 1️⃣ Data Collection
- Dataset: **Flight Delay and Cancellation Dataset (2019–2023)**
- Source: Kaggle
- Records: Over **3 million** entries, filtered to remove irrelevant and missing data.

### 2️⃣ Data Preprocessing
- Removed negative delay values and unnecessary columns  
- Extracted time-based features:  
  `Hour`, `Minute`, `DayOfWeek`, `IsWeekend`, and `TimePeriod`  
- Encoded categorical columns:  
  `AIRLINE`, `ORIGIN`, `DEST`, `DEP_TIME_PERIOD`  
- Scaled numerical features using **MinMaxScaler**  
- Split into **Train (70%)**, **Validation (20%)**, and **Test (10%)** sets

### 3️⃣ Model Development
Implemented and trained the following deep learning models:
- **Feedforward Neural Network (FNN)** – baseline model  
- **Simple RNN** – captures sequential dependencies  
- **LSTM** – handles long-term dependencies in sequences  
- **Bidirectional LSTM (BiLSTM)** – learns from both past and future context  

### 4️⃣ Model Evaluation
Each model was evaluated using:
- **Mean Absolute Percentage Error (MAPE)**
- **Accuracy**
- **Mean Absolute Error (MAE)**
- **R² Score**

---

## 📊 Results Summary

| Model | Developer | Accuracy | MAPE | R² Score | 
|:------|:-----------|:---------:|:------:|:--------:|
| **Feedforward Neural Network (FNN)** | [@chamodi54](https://github.com/chamodi54) | **98.14%** | **1.86%** | **0.9827** |
| **Simple RNN** | [@Tashika-Wijesooriya](https://github.com/Tashika-Wijesooriya) | **89.42%** | **10.58%** | — |
| **LSTM** | [@swiz9](https://github.com/swiz9) | **92.93%** | — | — |
| **Bidirectional LSTM (BiLSTM)** | [@vihangait22902252](https://github.com/vihangait22902252) | **93.31%** | — | — |

### 🧾 Key Insights
- **FNN** achieved the highest accuracy (**98.14%**) due to engineered features like *time-of-day* and *day-of-week*.  
- **RNN** performed moderately (**89.42% accuracy**) but struggled with long-term dependencies.  
- **LSTM** (**92.93% accuracy**) effectively captured long-term sequential patterns in flight delays.  
- **BiLSTM** (**93.31% accuracy**) slightly outperformed LSTM by learning from both *past* and *future* contexts.  
- **Sequential models (LSTM/BiLSTM)** provided better temporal understanding than FNN/RNN.  
- All models showed steady training and validation loss reduction, indicating **good learning stability**.  

---

## 🧩 Technologies Used
- **Python 3.x**
- **TensorFlow / Keras**
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Scikit-learn**
- **Google Colab**

---

## 👩‍💻 Contributors

| Name | GitHub |
|------|--------|
| [Tashika Wijesooriya](https://github.com/Tashika-Wijesooriya) |  RNN Model |
| [Anuradha Srimal](https://github.com/swiz9) |  LSTM Model |
| [Vihanga Wijesinghe](https://github.com/vihangait22902252) |  BiLSTM Model |
| [Chamodi](https://github.com/chamodi54) |  FNN Model |

---

## 🚀 Future Work
- Integrate weather and airport congestion data for higher accuracy  
- Deploy model as a web dashboard for real-time delay predictions  
- Experiment with Transformer-based sequence models  

---

## 📜 License
This project is licensed under the **MIT License**.  
Feel free to use, modify, and share with proper credit.

---

**⭐ Star this repo** if you find it helpful and want to support our project!
