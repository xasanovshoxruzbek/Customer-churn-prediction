# Customer Churn Prediction

Bank mijozlarining bank xizmatlaridan voz kechishini (churn) bashorat qilish loyihasi.

## Ma'lumotlar

Kaggle'dagi [Churn Modelling](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling) ma'lumotlar to'plami (10 000 mijoz). Notebook ma'lumotni to'g'ridan-to'g'ri internetdan yuklaydi.

## Jarayon

1. **Ma'lumotni tayyorlash:** NaN qiymatlarni tekshirish, `EstimatedSalary < 600` bo'lgan anomaliyalarni olib tashlash, `CustomerId` va `Surname` ustunlarini tashlab yuborish.
2. **Tahlil:** korrelyatsiya va heatmap.
3. **Train/test bo'linishi:** `Gender` bo'yicha `StratifiedShuffleSplit` (80/20).
4. **Preprocessing:** sonli ustunlar uchun `StandardScaler`, kategorik ustunlar (`Geography`, `Gender`) uchun `OneHotEncoder`.
5. **Modellar:** Logistic Regression, SVM, Decision Tree, Random Forest, XGBoost (sinflar nomutanosibligi hisobga olingan).
6. **Baholash:** Jaccard score, confusion matrix, classification report, ROC/AUC.

## Natija

Support Vector Machine va XGBoost boshqa modellarga nisbatan yaxshiroq natija ko'rsatdi.

## Ishga tushirish

```bash
pip install -r requirements.txt
jupyter notebook customer_churn_prediction.ipynb
```
