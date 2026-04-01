
from pathlib import Path
from textwrap import dedent

content = dedent("""\
# 🚗 Accident Risk Prediction (Kaggle)

🏆 **Kaggle Score:** `0.05559`

Bu projede, yol ve çevresel özelliklere bağlı olarak **kaza riski (`accident_risk`)** tahmini yapılmıştır.  
Çalışma, Kaggle yarışması kapsamında geliştirilmiş olup **ensemble tabanlı makine öğrenmesi yaklaşımı** kullanılmıştır.

---

## 🎯 Amaç

Bu projenin amacı:

- kaza riskini doğru tahmin etmek
- RMSE metriğini minimize etmek
- Kaggle leaderboard’da güçlü bir performans elde etmek

---

## 🏆 Sonuç

- **Best Kaggle Score:** `0.05559`
- **En iyi submission dosyası:** `submission_optimized.csv`

---

## 🧠 Kullanılan Yöntemler

### Base Modeller
- CatBoost
- LightGBM
- XGBoost

### Ensemble Yaklaşımı
- weighted averaging
- grid search ile optimum ağırlık seçimi

Örnek ağırlık dağılımı:
- CatBoost → ~0.25
- LightGBM → ~0.10
- XGBoost → ~0.65

### Ek Teknikler
- kategorik değişkenlerin uygun biçimde işlenmesi
- soft pseudo-labeling
- overfitting kontrolü için dengeli model yapısı

---

## 📁 Proje Yapısı

```bash
kaggle-kaza-riski/
│
├── notebooks/
│   └── kaggle_kaza_riski.ipynb
│
├── outputs/
│   └── submission_optimized.csv
│
├── data/
│   └── train.csv / test.csv / sample_submission.csv
│
├── README.md
├── requirements.txt
└── .gitignore



### VERİYİ https://www.kaggle.com/competitions/playground-series-s5e10/data burdaki linkten indirebilirsiniz.
