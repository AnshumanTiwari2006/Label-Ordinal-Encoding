# Label Encoding & Ordinal Encoding in Machine Learning

This notebook demonstrates how to convert categorical variables into numeric form using two common encoding techniques:
**Label Encoding** and **Ordinal Encoding**.

---

## 🧠 Why Encode Categorical Variables?

Machine learning algorithms require numeric input. Encoding techniques convert **non-numeric categorical data** into numbers so that models can process them.

---

## 🟢 Label Encoding

Label Encoding assigns a unique **integer** to each category.

### ✅ Use When:
- Categories **do not have an inherent order** (e.g., `Male`, `Female`)
- You’re using **tree-based models** that can handle arbitrary numerical assignments

### ⚠️ Caution:
Linear models may **misinterpret** the numerical relationship between encoded values as having an order.

---

## 🔵 Ordinal Encoding

Ordinal Encoding assigns integers **based on the order** or **rank** of categories.

### ✅ Use When:
- Categories **have a natural order** (e.g., `Low`, `Medium`, `High`)
- You want the model to **capture the relative ranking**

---

## 🛠️ Tools Used

- `pandas` for data manipulation
- `sklearn.preprocessing.LabelEncoder`
- `sklearn.preprocessing.OrdinalEncoder`

---

## 🚀 Example Usage

### Label Encoding:
```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()
df['Gender_encoded'] = le.fit_transform(df['Gender'])
