# Employee-Attrition

Proyek ini merupakan **Capstone Project Machine Learning** yang bertujuan untuk memprediksi apakah seorang karyawan akan **keluar dari perusahaan (Attrition)** atau **tetap bertahan**, berdasarkan data HR perusahaan.

Permasalahan attrition sangat penting karena tingginya tingkat keluar-masuk karyawan dapat meningkatkan biaya rekrutmen, pelatihan, serta menurunkan produktivitas perusahaan. Dengan model prediksi ini, perusahaan dapat mengambil langkah preventif untuk mempertahankan karyawan potensial.

## Tujuan Proyek

* Melakukan analisis data karyawan.
* Menangani data tidak seimbang (imbalanced data).
* Membangun beberapa model klasifikasi.
* Membandingkan performa model.
* Membuat model ensemble terbaik.
* Mengetahui faktor utama penyebab attrition.

## Dataset

Dataset yang digunakan:

**IBM HR Analytics Employee Attrition & Performance**

File:

`HR-Employee-Attrition.csv`

Target variabel:

* `Attrition`

  * Yes = Karyawan keluar
  * No = Karyawan bertahan

## 🛠️ Library yang Digunakan

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
imbalanced-learn
```

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```


## Tahapan Project

## Data Understanding

* Melihat ukuran dataset
* Mengecek tipe data
* Missing values
* Duplicate data

##  Data Cleaning

Kolom yang dihapus:

* EmployeeCount
* EmployeeNumber
* Over18
* StandardHours

Karena tidak memberikan informasi penting terhadap prediksi.

## Exploratory Data Analysis (EDA)

Visualisasi yang dilakukan:

* Distribusi Attrition
* OverTime vs Attrition
* Monthly Income vs Attrition
* Age Distribution

## Encoding

Semua kolom kategorikal diubah menjadi numerik menggunakan:

```python
LabelEncoder()
```

## Split Data

```python
80% Training
20% Testing
```

Menggunakan stratify agar proporsi target tetap seimbang.

## Handling Imbalanced Data

Menggunakan:

```python
SMOTE
```

Untuk menyeimbangkan jumlah kelas Attrition.

##  Feature Scaling

Menggunakan:

```python
StandardScaler
```

Digunakan untuk model:

* Logistic Regression
* KNN
* SVM
* Neural Network

---

# Model Machine Learning

Model yang diuji:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. AdaBoost
5. Gradient Boosting
6. K-Nearest Neighbors
7. Support Vector Machine
8. Neural Network (MLP)



# Evaluation Metrics

Menggunakan:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC AUC

Karena data imbalance, fokus utama evaluasi menggunakan:

 **F1 Score**

# 🏆 Ensemble Learning

Menggunakan **Soft Voting Classifier** dengan kombinasi:

* Random Forest
* Gradient Boosting
* AdaBoost

```python
VotingClassifier(voting='soft')
```


#  Visualisasi Hasil

Project menghasilkan visualisasi:

* Perbandingan F1 Score tiap model
* Confusion Matrix
* ROC Curve
* Feature Importance



# Feature Importance

Variabel yang paling berpengaruh terhadap attrition biasanya:

* OverTime
* MonthlyIncome
* Age
* JobSatisfaction
* YearsAtCompany



#  Hasil Akhir

Model terbaik dipilih berdasarkan **F1 Score**, umumnya:

* Voting Ensemble
* Random Forest
* Gradient Boosting

Cross Validation juga dilakukan untuk memastikan model stabil.

---

# Cara Menjalankan Project

```bash
git clone https://github.com/username/repository-name.git
cd repository-name
python employee_attrition.py
```

Atau jalankan melalui Jupyter Notebook.

---

#  Struktur Folder

```bash
├── HR-Employee-Attrition.csv
├── employee_attrition.py
├── README.md
```

---

# Insight Bisnis

Perusahaan dapat fokus mempertahankan karyawan dengan karakteristik:

* Sering lembur
* Gaji rendah
* Kepuasan kerja rendah
* Masa kerja pendek
* Usia muda

Dengan strategi retensi yang tepat, attrition dapat ditekan.

# ⭐ Jika project ini bermanfaat, jangan lupa beri star repository ini.
