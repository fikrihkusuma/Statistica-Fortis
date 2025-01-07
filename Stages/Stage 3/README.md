# Stage 3
## Modeling
### Split data
Kami melakukan split data training 80% dan test 20%
### Modeling
Model yang kami coba adalah ‘Decision Tree’, ‘Random Forest’, ‘SVM Kernel Poly’, ‘KNN’, dan ‘XGBOOST’
### Model Evaluation
Metrics yang kami gunakan untuk mengevaluasi model kami adalah ‘akurasi’, ‘precision’, ‘recall’, dan ‘F1-score’
### Hyperparameter Tuning
Kami melakukan hyperparameter tuning untuk semua model yang kami coba, berikut adalah contoh hyperparameter tuning untuk model random forest kami: <br>

param_grid = { <br>
    'n_estimators': [50, 100, 200],      Jumlah pohon dalam hutan <br>
    'max_depth': [None, 10, 20, 30],     Kedalaman maksimum pohon <br>
    'min_samples_split': [2, 5, 10],     Jumlah minimum sampel untuk membagi node <br>
    'min_samples_leaf': [1, 2, 4],       Jumlah minimum sampel di setiap daun <br>
    'criterion': ['gini', 'entropy']     Kriteria pemisahan <br>

### Eksperimen
Kami bereksperimen dengan preprocessing hingga splitting data kami, berikut adalah skenarionya: <br>
Percobaan 1 : <br>
Drop outlier -> StandarScaler semua fitur selain target -> split data train dan test <br>
Percobaan 2 : <br>
Drop outlier -> split data train dan test -> Baru fitur2nya dilakukan StandarScaler <br>
Percobaan 3 : <br>
Tanpa drop outlier -> StandarScaler semua fitur -> split data train dan test <br>
Percobaan 4 : <br>
Tanpa drop outlier -> split data train dan test -> Baru fitur2nya dilakukan StandarScaler <br>

## Feature Importance
Kami melakukan feature importance dengan decision tree, dengan mengurutkan hasil dari yang paling penting, berikut adalah 5 fitur teratas (paling penting): <br>
‘MonthlyIncome’		: 0.1109 <br>
‘Age’			: 0.0802 <br>
‘DistanceFromHome’	: 0.0733 <br>
‘TotalWorkingYears’	: 0.0592 <br>
‘PercentSalaryHike’	: 0.0550
