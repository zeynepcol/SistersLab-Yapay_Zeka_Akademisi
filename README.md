# 🫀 Kalp Hastalığı Risk Analizi (Heart Disease UCI) 🫀

### 🧠 SistersLab Yapay Zeka Akademisi Bitirme Projesi

Bu proje, SistersLab Yapay Zeka Akademisi bitirme projesi kapsamında oluşturulmuştur.

## 📌 Proje Özeti

Kalp hastalığı riskini tahmin etmeye yönelik bu projede, **Heart Disease - UCI** veri seti kullanılmıştır. Amaç, bireylerin kalp hastalığı riski taşıyıp taşımadığını makine öğrenmesi modelleri ile tahmin ederek erken teşhis olanaklarını artırmak ve sağlık sistemine katkı sağlamaktır.

> 📁 Veri Seti Kaynağı: [Heart Disease UCI – Kaggle](https://www.kaggle.com/datasets/mragpavank/heart-diseaseuci)  
> 🎯 Hedef Değişken: `target`  
> - `target = 1` → Kalp hastalığı riski var  
> - `target = 0` → Kalp hastalığı riski yok

Bu çalışma ile:  
✅ Erken teşhis sağlanabilir  
✅ Sağlık sistemi üzerindeki yük hafifletilebilir  
✅ Toplum sağlığı korunabilir

---

## 🔍 1. Problem Tanımı

- **Veri seti**: Heart Disease - UCI  
- **Kullanım amacı**: Kalp hastalığı riski taşıyan bireyleri sınıflandırmak (`0` veya `1`)
- **Toplam gözlem**: 303  
- **Özellik sayısı**: 14  

---

## 📊 2. Veri Analizi ve Görselleştirme (EDA)

- `df.info()` ve `df.describe()` ile temel incelemeler yapıldı.
- Eksik veri bulunmamaktadır.
- Hedef değişken dengeli bir dağılıma sahiptir.
- Görselleştirilen değişkenler:
  - `age`, `sex`, `cp`, `trestbps`, `chol`, `thalach`, vb.
- Korelasyon analizi ile değişken ilişkileri incelendi.

---

## ⚙️ 3. Veri Ön İşleme

- **Etiket Kodlama (Label Encoding):** `sex`, `fbs`, `exang`
- **One-Hot Kodlama (OneHotEncoding):** `cp`, `restecg`
- **Ölçeklendirme:** Sayısal veriler `StandardScaler` ile normalize edildi.
- **Veri Ayrımı:** `%80` Eğitim / `%20` Test (`train_test_split(test_size=0.2)`)

---

## 🤖 4. Modelleme

İki farklı sınıflandırma modeli uygulandı:

| 📌 Model              | 🎯 Accuracy | 🎯 Precision | 📈 Recall | ⚖️ F1-Score | 📉 ROC-AUC |
|----------------------|-------------|--------------|-----------|--------------|-------------|
| Logistic Regression  | 0.85        | 0.90         | 0.81      | 0.85         | 0.93        |
| Random Forest        | 0.82        | 0.84         | 0.81      | 0.83         | 0.92        |

- 📉 **ROC Eğrisi**  
- 📊 **Confusion Matrix** ile değerlendirme yapıldı  
- ✅ **En dengeli model:** Logistic Regression

---

## 🆚 5. Model Karşılaştırması

- 🏆 **Başarılı Model:** Logistic Regression  
- 📌 **Öne Çıkan Metrik:** Precision  
- 🚫 **Overfitting veya Underfitting** gözlenmedi  
- ✅ Test performansı yüksek ve dengeli

---

## ✅ 6. Sonuç ve Yorumlar

- Logistic Regression modeli, doğruluk ve ROC-AUC metriklerinde daha başarılı oldu  
- Random Forest modeli destekleyici ve alternatif model olarak değerlendirildi  

---
## 🙏 Teşekkürler

Yapay Zeka Akademisi süresince kazandığım bilgi, deneyim ve ilham için teşekkür ederim.  
Başta değerli eğitmenimiz **Yasemin Arslan** olmak üzere, tüm **SistersLab proje asistanlarına** ve emeği geçen herkese gönülden teşekkür ederim.  
Teknik donanımın yanı sıra ilham verici bir öğrenme ortamı sunduğunuz için minnettarım.

---
> Proje sahibi: [Zeynep ÇÖL](https://www.linkedin.com/in/zeynep-col/)
