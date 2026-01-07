
# UAS II3160 - Mengembangkan Layanan Microservice (Tugas 3)
<p align="center">
  <img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/037e90f0-c3fe-4f33-9c9f-2d184dfb051b" />
</p>

## Mealy: Diet Meal Planner
Microservice ini dikembangkan dalam rangka memenuhi UAS II3160 Teknologi Sistem Terintegrasi, lebih tepatnya Tugas 3 - Integrasi Layanan 
- Nama Pembuat Layanan Integrasi: Favian Rafi Laftiyanto / 18223036
- Nama Rekan Sekelompok yang Dimanfaatkan API-nya: Ahmad Evander Ruizhi Xavier / 18223064

### A. Deskripsi
Mealy adalah aplikasi Diet Meal Planner yang dirancang untuk membantu pengguna menentukan pilihan makanan sehat berdasarkan profil kesehatan personal. Aplikasi ini menghitung kebutuhan nutrisi harian (BMR, BMI, dan Calorie Needs) serta memberikan rekomendasi makanan yang telah difilter sesuai dengan batasan medis tertentu. Layanan dapat diakses pada: https://19623238-favian.github.io/mealy/ (GitHub Pages) atau https://mealy.cirro.my.id/ (VPS VM Azure)

Layanan ini dikembangkan dengan memanfaatkan 2 buah API yang telah dibuat pada Tugas sebelumnya (Tugas 2). Berikut adalah API yang dimanfaatkan pada layanan ini:
- [API Healthy Grocery](https://github.com/19623238-Favian/API-Healthy-Grocery) : https://api.cirro.my.id/api/recommendation/food
  - Digunakan untuk menentukan BMI, BMR, dan kebutuhan nutrisi pengguna
- [API Nutrient](https://github.com/evanderruizhi2/nutrition-serviceAPI.git) : https://evanrzh.theokaitou.my.id/api/nutrition/constraints
  - Digunakan untuk menentukan rekomendasi makanan sehat bagi pengguna dan juga untuk mencari kandungan nutrisi suatu makanan

### B. Fitur Utama
- **Personalized Health Calculator**: Menghitung BMI (Body Mass Index) dan BMR (Basal Metabolic Rate) secara otomatis berdasarkan usia, berat badan, tinggi badan, dan tingkat aktivitas.
- **Medical Condition Filtering**: Memberikan batasan nutrisi khusus (seperti batas gula, natrium, atau lemak) bagi pengguna dengan kondisi medis seperti Diabetes, Hipertensi, dan Penyakit Jantung.
- **Healthy Food Recommendations**: Menampilkan 5 + 10 menu makanan terbaik dengan skor kesehatan tertinggi yang paling sesuai dengan kebutuhan pengguna.
- **Search & Sort Nutrition**: Fitur pencarian database makanan yang dilengkapi dengan fungsi pengurutan (*sorting*) berdasarkan kandungan nutrisi (Kalori, Protein, Karbohidrat, dll).

### C. Technology Stack yang Digunakan
- **Frontend**: HTML5, Tailwind CSS, JavaScript (Vanilla JS).
- **Icons**: Font Awesome 6.0.
- **API Backend**: 
  - `https://evanrzh.theokaitou.my.id/api` (Nutrition Constraints)
  - `https://api.cirro.my.id` (Food Recommendation)
- **Deployment**: GitHub Pages dan Azure Virtual Machine (2 versi berbeda)

### D. Cara Kerja Aplikasi
1. **Access Key Authentication**: Pengguna harus memasukkan access key "Mealy-UAS-TST2025" ke website Mealy untuk dapat sepenuhnya menggunakan fitur-fitur Mealy.
2. **Input Data**: Pengguna memasukkan data fisik dan memilih riwayat kondisi medis.
3. **Analisis Nutrisi**: Aplikasi mengirim data ke API untuk mendapatkan kalkulasi batasan nutrisi (Constraints).
4. **Pencocokan Data**: Algoritma aplikasi memfilter database makanan yang ada di API untuk mencari menu yang tidak melanggar batasan nutrisi pengguna.
5. **Scoring**: Makanan diurutkan berdasarkan skor kesehatan untuk memberikan rekomendasi yang paling optimal.

### E. Screenshot Website
#### Access Key Authentication Page


#### Main Page
<img width="1600" height="765" alt="image" src="https://github.com/user-attachments/assets/049359dd-4ac0-4c21-99ad-f57e77e28a3e" />
<img width="1600" height="767" alt="image" src="https://github.com/user-attachments/assets/791c468c-8012-4a32-a687-c5a422e0d927" />

#### Food Recommendations Example
<img width="1600" height="770" alt="image" src="https://github.com/user-attachments/assets/fb16964d-1214-43da-90fd-37e093b4c532" />
<img width="1600" height="766" alt="image" src="https://github.com/user-attachments/assets/fc9c46bc-80b0-41f7-ac0d-7ad4588b14c3" />


#### Food Nutritions Search
<img width="1600" height="759" alt="image" src="https://github.com/user-attachments/assets/54739359-d67c-46db-9ca4-5363f187061a" />
<img width="1600" height="766" alt="image" src="https://github.com/user-attachments/assets/e67fcc5c-de6d-4ae6-bf01-ddf881797748" />
