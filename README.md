# 🎓 Student Exam Score Prediction

> A beginner-to-intermediate Python + Machine Learning practice project using Linear Regression.

---

## 📌 Problem Statement

Can we predict a student's exam score based on their study habits and attendance?  
This project builds a Linear Regression model to answer that question using a custom dataset.

---

## 📊 Dataset Description

- **Size:** 20 rows × 4 features
- **Created manually** using domain knowledge

| Feature | Description |
|---|---|
| `hours_studied` | Hours spent studying per day |
| `attendance_pct` | Class attendance percentage (0–100) |
| `prev_score` | Score in the previous exam |
| `exam_score` | 🎯 **Target** — Score to predict |

---

## 🤖 Model Used

**Linear Regression** (from `scikit-learn`)

- Train/Test Split: 80% train, 20% test
- Random State: 42

---

## 📈 Results

| Experiment | MAE | R² |
|---|---|---|
| Baseline (`hours + attendance`) | ~3.5 | ~0.96 |
| Only `hours_studied` | ~4.2 | ~0.94 |
| + `prev_score` added | ~1.8 | ~0.99 |

### Key Findings:
- `prev_score` is the **most predictive** feature
- Removing `attendance_pct` slightly hurts performance
- Overfitting observed when training on full data without a split

---

## 📂 Project Structure

```
├── student_exam_score_prediction.ipynb   # Main notebook
├── scatter_plot.png                      # Visualization 1
├── histogram.png                         # Visualization 2
├── boxplot.png                           # Visualization 3
└── README.md                             # This file
```

---

## 🛠️ Libraries Used

- `pandas` — Data manipulation
- `numpy` — Numerical operations
- `matplotlib` — Visualization
- `scikit-learn` — ML model, metrics, train-test split

---

## ✅ Conclusion

- Linear Regression performs well on this structured dataset
- Previous exam score (`prev_score`) is the strongest predictor
- Proper train-test splitting is **essential** to avoid overfitting
- More data and additional features (sleep hours, stress level) could further improve the model

---

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/student-exam-score-prediction
cd student-exam-score-prediction
pip install pandas numpy matplotlib scikit-learn notebook
jupyter notebook student_exam_score_prediction.ipynb
```
