1. Descriptive statistics
Semua tipe data sudah sesuai dengan ekspektasi untuk dataset ini. Kolom numerik dan kategorikal memiliki tipe data yang tepat, seperti int64 dan object untuk kategori.
Ada beberapa kolom yang memiliki nilai kosong:
-NumCompaniesWorked: 19 nilai kosong
-TotalWorkingYears: 9 nilai kosong
-EnvironmentSatisfaction: 25 nilai kosong
-JobSatisfaction: 20 nilai kosong
-WorkLifeBalance: 38 nilai kosong

Beberapa observasi dari nilai summary:
-Kolom EmployeeCount hanya memiliki nilai 1 untuk semua baris, sehingga mungkin kurang informatif dan bisa diabaikan dalam analisis.
-Kolom StandardHours juga menunjukkan nilai yang sama (80) untuk semua baris, sehingga kurang bervariasi dan bisa dipertimbangkan untuk tidak dimasukkan ke dalam model analisis jika tidak relevan.
-Kolom PerformanceRating hanya memiliki dua nilai unik, 3 dan 4, dengan mayoritas berada di nilai 3, yang mungkin perlu dianalisis lebih lanjut untuk memahami distribusinya.

2. Univariate analysis
-Kolom yang memiliki outier antara lain YearsWithCurrManager, YearsSinceLastPromotion, YearsAtCompany, TrainingTimesLastYear, TotalWorkingYears, dan MonthlyIncome
-WorkLifeBalance, JobInvolvement, TrainingTimesLastYear, Education, dan Age memiliki persebaran normal.
-JobSatisfaction dan EnvironmentSatisfaction memiliki persebaran negative skewed
-YearsSinceLastPromotion, YearsAtCompany, TotalWorkingYears, PercentSalaryHike, NumCompanyWorked, MonthlyIncome, JobLevel, dan DistanceFromHome memiliki persebaran positive skewed
-YearsWithCurrManager memiliki persebaran bimodal

3. Multivariate analysis
-Kolom PercentSalaryHike, StockOptionLevel, dan Performance rating berkorelasi 3-4% dengan target (Job satisfaction)
-Kolom MonthlyIncome dan JobInvolvement berkorelasi lemah yaitu 0.3% dengan target (Job satisfaction)
-PerformanceRating dengan PercentSalaryHigh berkorelasi positif 77%, tidak cukup tinggi untuk dihapus salah satunya

4. Business insight
-Job Satisfaction & Environment Satisfaction
 -Insights:
Negative skewness pada JobSatisfaction dan EnvironmentSatisfaction menunjukkan bahwa kebanyakan karyawan memiliki tingkat kepuasan tinggi, tapi ada sekelompok karyawan yang tidak memiliki tingkat kepuasan yang tinggi.
 -Recommendation:
Lakukan riset terhadap karyawan kenapa ada sekelompok karyawan yang memiliki kepuasan yang rendah
-Hubungan Salary Hike
 -Insights:
Feature PercentSalaryHike dan PerformanceRating menunjukkan skor korelasi sebesar 77%, menunjukkan hubungan yang cukup signifikan antara kedua feature tersebut, hal ini juga bisa saja menunjukkan bahwa struktur upah pada WOMart mungkin sangat berdasarkan performa kerja.
 -Recommendation:
Tingkatkan efektivitas program yang mendukung peningkatan gaji dengan performa kerja.
-Faktor yang berhubungan dengan JobSatisfaction:
 -Insights:
feature MonthlyIncome dan PercentSalaryHike menunjukkan hubungan yang lemah dengan JobSatisfaction.
 -Recommendation:
Tim HR bisa menelaah teknik pengumpulan data, apakah sudah benar atau belum, jika memang sudah benar tim HR mungkin bisa melakukan riset terhadap faktor lain yang mungkin memengaruhi kepuasan kerja karyawannya.
