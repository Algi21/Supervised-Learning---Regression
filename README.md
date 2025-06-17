# Supervised---Regression
Project supervised learning dengan Model Regression untuk memprediksi jumlah views youtube berdasarkan dataset (https://docs.google.com/spreadsheets/d/1udQirplaI0mAGJnuZPlPHPaxr7RtisYt/export?format=csv&gid=1632283680)

# Overviews
Goals : Memprediksi jumlah views di youtube berdasarkan fitur-fitur pada dataset yang dipilih <br>
Business Impact : Untuk menentukan strategy enggangement dan cara meningkatkan jumlah views bagi pengguna youtube

# Exploratory Data Analysis
- Deskripsi Statistik data numerical dan kategorical
- Univariate Analysis : Boxplot, KDE Plot
- Multivariate Analysis : Heatmap

# Data Preprocessing
- Handling missing value dan duplikat: Dropped Nan
- Handling Outliers : Metode IQR
- Feature Engineering : publish_hour, is_weekend
- Feature Selection : Metode ANOVA
- Scalling dan transform data : Metode RobustScaler

# Training & Evaluasi Model
- Data Splitting : Data Train (80%) dan Data Test (20%)
- Baseline Model : LinearRegression
- Model Evaluated : RandomForestRegressor, XGBRegressor

# Hyperparameter Turning
- Approach :
  - GridSearchCV (RandomForestRegressor)
  - RandomizedSearchCV (XGBRegressor)
- Scoring: Root Mean Squared Error (RMSE) dan R-squared (R²)

# Kesimpulan
1.   Dalam kondisi model tanpa hyperparameter tuning, akurasi model Random Forest Regressor mengalahkan model Linier Regression dan Gradient Boosting Regressor.<br>
Dimana nilai RMSE dan R² untuk  Random Forest Regressor, Linier Regression dan Gradient Boosting Regressor masing-masing sebesar:<br>
[0.55, 0.70], [0.68, 0.54], [0.56, 0.69]
2.   Dari model-model tersebut di pilih 2 model untuk dilakukan hyperparameter tuning untuk meningkatkan akurasi dari model, yaitu Random Forest Regressor, dan Gradient Boosting Regressor dengan pertimbangan utama nilai RMSE yang kecil dan R² yang diatas 0.65. <br>
Dengan hasil akurasi RMSE dan R² setelah hyperparameter tuning berturut-turut untuk Random Forest Regressor, dan Gradient Boosting Regressor sebesar:<br>
[0.55, 0.70], [0.50, 0.75]
3.   Hasil hyperparameter tuning dari Random Forest Regressor tidak menunjukkan perubahan akurasi, sedangkan hasil hyperparameter tuning dari Gradient Boosting Regressor menunjukkan peningkatan akurasi yang lumayan dimana RMSE dari 0.56 menjadi 0.50 dan R² dari 0.69 menjadi 0.75
4.   Berdasarkan ini, untuk pemodelan prediksi jumlah viewer Youtube lebih bisa diwakili oleh model Gradient Boosting Regressor yang sudah dilakukan hyperparameter tuning


