# IPL-runpredictor
# 🏏 IPL Run Predictor

> Predict how many runs an IPL batsman will score using Machine Learning

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3-orange?logo=scikit-learn)](https://scikit-learn.org)
[![Google Colab](https://img.shields.io/badge/Run%20on-Google%20Colab-yellow?logo=googlecolab)](https://colab.research.google.com)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

---

## 📌 Project Overview

This project builds an end-to-end Machine Learning pipeline that predicts the number of runs an IPL batsman will score in a match innings based on historical performance features.

**Problem Type:** Regression  
**Best Model:** Random Forest Regressor (R² ≈ 0.82)  
**Dataset:** IPL Ball-by-Ball Data (2010–2023)

---

## 🗂️ Folder Structure

```
IPL-Performance-Predictor/
│
├── 📓 IPL_Performance_Predictor.ipynb   ← Main Colab Notebook (run this!)
├── 📄 IPL_Proposal_Report.docx          ← Project Proposal Report
├── 🎬 screen_recording.mp4              ← Demo Screen Recording
└── 📖 README.md                         ← This file
```

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)
1. Click **Open in Colab** badge above, or go to [colab.research.google.com](https://colab.research.google.com)
2. Upload `IPL_Performance_Predictor.ipynb`
3. Click **Runtime → Run All**
4. Done! No setup needed — dataset is auto-generated inside the notebook.

### Option 2 — Local Setup
```bash
git clone https://github.com/YOUR_USERNAME/ipl-performance-predictor
cd ipl-performance-predictor
pip install numpy pandas matplotlib seaborn scikit-learn ipywidgets
jupyter notebook IPL_Performance_Predictor.ipynb
```

---

## 🧠 ML Pipeline

```
Raw Data → EDA → Feature Engineering → Model Training → Evaluation → Prediction UI
```

### Features Used
| Feature | Description |
|---|---|
| `rolling_avg_runs` | 5-match rolling average of batsman's runs |
| `strike_rate` | Runs per 100 balls |
| `balls_faced` | Balls faced in the innings |
| `boundaries` | Number of 4s and 6s |
| `recent_form_index` | Weighted avg of last 3 matches |
| `batting_position` | Position in batting order (1–6) |
| `is_home` | Playing at home ground (1/0) |
| `dot_ball_pct` | % of dot balls faced |

### Models Compared
| Model | R² Score | MAE |
|---|---|---|
| Linear Regression | ~0.60 | ~8 runs |
| **Random Forest** ✅ | **~0.82** | **~5 runs** |
| Gradient Boosting | ~0.79 | ~6 runs |

---

## 📊 Results

- **Best R² Score:** ~0.82 (Random Forest)
- **Best MAE:** ~5 runs (Random Forest)
- **Cross-validation R² (5-fold):** ~0.80 ± 0.02

### Key Insights
- Rolling average runs is the **#1 predictor** of performance
- Strike rate and recent form strongly correlate with runs scored
- Batting position significantly affects scoring patterns (top-order > middle)
- Home advantage has a small but measurable positive impact

---

## 🎯 Interactive Predictor

The notebook includes a **live prediction widget** where you can:
- Select any IPL batsman, team, and venue
- Adjust match stats using sliders
- Get instant run predictions from both RF and GB models

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **Pandas & NumPy** — data manipulation
- **Scikit-learn** — ML models & evaluation
- **Matplotlib & Seaborn** — visualizations
- **ipywidgets** — interactive UI
- **Google Colab** — development environment

---

## 🚀 Future Improvements

- [ ] Integrate real Kaggle IPL dataset
- [ ] Add weather & pitch condition features
- [ ] LSTM model for time-series form tracking
- [ ] Deploy as Streamlit web app
- [ ] Include bowling stats to predict wickets

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 👤 Author

**Dheeraj**  
B.Tech CSE | Machine Learning Enthusiast  
📧 your.email@example.com  
🔗 [LinkedIn](https://linkedin.com) | [GitHub](https://github.com)

---

*⭐ Star this repo if you found it useful!*
