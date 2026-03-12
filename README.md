# Kredi-Karti-Sahtekarlik-Tespiti

[![TR](https://img.shields.io/badge/Lang-TR-red.svg)](#türkçe) [![EN](https://img.shields.io/badge/Lang-EN-blue.svg)](#english)

---

## 🇹🇷 Türkçe

### Proje Hakkında
Bu proje, kredi kartı işlemlerinin sahte (fraud) olup olmadığını tespit etmek amacıyla geliştirilmiş bir makine öğrenmesi çalışmasıdır. Çalışmada Yapay Sinir Ağları (YSA), XGBoost ve Random Forest modelleri karşılaştırmalı olarak incelenmiş ve gerçek dünya problemlerinden biri olan "dengesiz veri seti" (imbalanced data) sorunuyla başa çıkmak için çeşitli teknikler uygulanmıştır.

### Veri Seti ve Ön İşleme
- **Kaynak:** Kaggle - Credit Card Fraud Detection
- **Veri Yapısı:** Toplam 284,807 işlem kaydı ve PCA ile dönüştürülmüş 30 sayısal özellik.
- **Dengesizlik Durumu:** Sahte işlemler, tüm veri setinin yalnızca **%0.17'sini** oluşturmaktadır (492 sahte işlem).
- **Ön İşleme:** Eksik veri bulunmayan setteki tüm özellikler `StandardScaler` ile ölçeklendirilmiş; dengesiz sınıf problemi **SMOTE** (Synthetic Minority Over-sampling Technique) yöntemiyle çözülmüştür.

### Kullanılan Modeller
1. **Yapay Sinir Ağları (YSA - ANN)**
2. **XGBoost**
3. **Random Forest**

### Bulgular ve Sonuç
- Modeller arasında en yüksek performansı **Random Forest** modeli göstermiştir. Özellikle modelin 'balanced' modu dengesiz veriyle başa çıkmada en etkili yöntem olmuştur.
- **XGBoost**, hız ve performans açısından en iyi dengeyi sunarak pratik uygulamalar için güçlü bir alternatif olduğunu kanıtlamıştır.
- **YSA**, diğerlerine göre nispeten daha düşük performans gösterse de ROC-AUC değeri açısından yüksek bir skor elde etmiştir.
- Genel olarak SMOTE tekniğinin uygulanması, tüm modellerin *Recall* (Duyarlılık) değerlerinde belirgin bir iyileşme sağlamıştır.

### Dosya Yapısı
- [**KrediKartıSahtekarlıkKodlar.ipynb**](./KrediKartıSahtekarlıkKodlar.ipynb): Veri ön işleme, SMOTE uygulaması, model eğitimleri ve performans metriklerinin (özellik önemlilikleri, grafikler vb.) yer aldığı Python Notebook dosyası.
- [**Kredi_Karti_Sahtekarlik_Tespiti.pdf**](./Kredi_Karti_Sahtekarlik_Tespiti.pdf): Projenin problemini, yöntemlerini, analiz bulgularını ve gelecek çalışmalar için önerileri içeren detaylı rapor.

---

## 🇬🇧 English

### About the Project
This project is a machine learning study developed to detect whether credit card transactions are fraudulent. The study comparatively examines Artificial Neural Networks (ANN), XGBoost, and Random Forest models, applying various techniques to tackle the real-world problem of "imbalanced datasets."

### Dataset & Preprocessing
- **Source:** Kaggle - Credit Card Fraud Detection
- **Data Structure:** A total of 284,807 transaction records and 30 numerical features transformed via PCA.
- **Imbalance:** Fraudulent transactions make up only **0.17%** of the entire dataset (492 fraudulent transactions).
- **Preprocessing:** All features in the dataset (which contained no missing values) were scaled using `StandardScaler`. The class imbalance problem was addressed using the **SMOTE** (Synthetic Minority Over-sampling Technique) method.

### Models Used
1. **Artificial Neural Networks (ANN)**
2. **XGBoost**
3. **Random Forest**

### Findings & Conclusion
- The **Random Forest** model demonstrated the highest overall performance. Specifically, the model's 'balanced' mode was the most effective method for handling the imbalanced data.
- **XGBoost** provided the best balance between speed and performance, proving to be a strong alternative for practical applications.
- Although **ANN** showed relatively lower performance compared to the others, it still maintained a high ROC-AUC score.
- Overall, the application of the SMOTE technique provided a significant improvement in the *Recall* values across all models.

### Repository Structure
- [**KrediKartıSahtekarlıkKodlar.ipynb**](./KrediKartıSahtekarlıkKodlar.ipynb): The Python Notebook containing data preprocessing, SMOTE application, model training, and performance metrics (feature importances, visualizations, etc.).
- [**Kredi_Karti_Sahtekarlik_Tespiti.pdf**](./Kredi_Karti_Sahtekarlik_Tespiti.pdf): The detailed report covering the project problem, methodology, analysis findings, and recommendations for future work.
