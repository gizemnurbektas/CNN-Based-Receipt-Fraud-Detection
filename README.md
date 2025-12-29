# CNN-Based-Receipt-Fraud-Detection
# CNN-Based Receipt Fraud Detection (Real vs Fake)

Bu proje, fiş/dekont görüntülerinde **manipülasyon veya sahtecilik şüphesi** olup olmadığını tespit etmek amacıyla geliştirilmiş **CNN tabanlı bir görüntü sınıflandırma uygulamasıdır**.  
Model, **gerçek (REAL)** ve **üzerinde oynanmış / karalanmış (FAKE)** fiş görselleriyle eğitilmiş ve **Gradio** arayüzü üzerinden canlı olarak test edilebilmektedir.

---

## Proje Amacı
Bankacılık ve finans alanında sık karşılaşılan sahte belge problemlerine yönelik olarak, fiş ve dekont görüntülerinde yapılan görsel manipülasyonları otomatik şekilde tespit edebilen bir derin öğrenme modeli geliştirmek.

---

## Kullanılan Teknolojiler
- Python
- PyTorch
- Convolutional Neural Networks (CNN)
- OpenCV
- Gradio

---

## Girdi / Çıktı
- **Girdi:** Fiş veya dekont görseli (JPG / PNG)
- **Çıktı:**  
  - `REAL (Orijinal)`  
  - `FAKE (Manipülasyon Şüphesi)`  
  - Güven skoru (olasılık)

---

## Klasör Yapısı
Proje aşağıdaki klasör yapısını kullanır:
receipt_fraud_cnn/
│
├── model.py # CNN model mimarisi
├── train.py # Model eğitim kodu
├── serve.py # Gradio arayüzü
│
├── cnn_model.pth # Eğitilmiş model (train sonrası oluşur)
│
└── data/
└── receiptimages/
├── real/ # Orijinal fiş görselleri
└── fake/ # Karalanmış / oynanmış fiş görselleri


---

## Kurulum
Proje **Google Colab** üzerinde çalıştırılacak şekilde tasarlanmıştır.


