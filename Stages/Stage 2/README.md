# Stage 2
## Membuang Fitur
Kami membuang fitur yang kami anggap tidak akan begitu berdampak pada performa model, yaitu <br>
'EmployeeID', 'StandardHours', 'EmployeeCount'
## EDA
### Missing Values
Terdapat missing values pada beberapa fitur:
NumCompaniesWorked	: 19 nilai kosong <br>
TotalWorkingYears	: 9 nilai kosong <br>
EnvironmentSatisfaction	: 25 nilai kosong <br>
JobSatisfaction		: 20 nilai kosong <br>
WorkLifeBalance		: 38 nilai kosong <br>

### Duplicate Data
Tidak ada duplicate data
### Outliers
Kolom atau fitur yang memiliki outier antara lain “YearsWithCurrManager”, “YearsSinceLastPromotion”, “YearsAtCompany”, “TrainingTimesLastYear”, “TotalWorkingYears”, dan “MonthlyIncome”.<br> 
Kami belum menentukan akan handle outliers tersebut seperti apa, karena dari model yang akan kami coba, yaitu random forest, model tersebut robust terhadap outliers.
## Univariate Analysis
Rata-rata sebaran data pada tiap fitur mengalami kemiringan
## Multi Variate Analysis
Ada beberapa fitur yang mengalami multikolinearitas: <br>
'TotalWorkingYears' dengan 'Age', 'YearsAtCompany' <br>
'YearsAtCompany' dengan 'YearSinceLastPromotion', 'YearsWithCurrManager'
## Transformasi Fitur
Kami melakukan transformasi fitur kategori menggunakan one-hot encoder, fitur yang kami transformasi adalah: <br>
'Attrition', 'BusinessTravel', 'Department', 'EducationField', 'Gender', 'JobRole', 'MaritalStatus'