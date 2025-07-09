# Text_Sentiment_Analysis

Bu proje, farklı kaynaklardan elde edilen metin verileri üzerinde **duygu analizi (sentiment analysis)** yapmak için geliştirilmiştir.  
Proje kapsamında metinlerin temizlenmesi, sayısallaştırılması (embedding), ardından farklı derin öğrenme mimarileri (CNN, LSTM, GRU) ile sınıflandırılması sağlanmıştır.

---

## 🚀 Proje Özeti

- **Veri Setleri:**
  - IMDB film yorumları
  - Amazon ürün yorumları
  - Sentiment140 (Twitter) tweet verileri

- **Kullanılan Modeller:**
  - CNN
  - LSTM
  - GRU

- **Çıktılar:**
  - Eğitimli modeller (`.keras` formatında)
  - İşlenmiş ve temizlenmiş CSV verileri
  - Analiz ve eğitim için Jupyter notebook dosyaları

---

## 📂 Klasör Yapısı

```
Text_Sentiment/
│
├── best_cnn.keras
├── best_rnn.keras
├── best_lstm.keras
├── best_gru.keras
│
├── prepare_amazon.ipynb
├── prepare_imdb.ipynb
├── prepare_sentiment140.ipynb
│
├── README.md
```

---

## ⚙️ Kullanılan Teknolojiler

- Python 3.10+
- Pandas, Numpy
- TensorFlow & Keras
- Matplotlib, Seaborn
- NLTK (stopwords, tokenization)
- Jupyter Notebook

---

## 🛠️ Uygulanan İş Akışı

Bu proje aşağıdaki temel aşamalardan oluşmaktadır:

- **Veri Temizleme:**  
  Metinler küçük harfe dönüştürülmüş, sayılar ve noktalama işaretleri temizlenmiş; opsiyonel olarak stopword çıkarma ve lemmatizasyon işlemleri uygulanmıştır.

- **Sayısallaştırma & Embedding:**  
  Metin verileri tokenizer yardımıyla dizilere dönüştürülmüş, ardından embedding katmanı ile kelimeler vektör uzayında temsil edilmiştir.

- **Modelleme:**  
  CNN, LSTM ve GRU gibi farklı derin öğrenme mimarileri ile sentiment sınıflandırması gerçekleştirilmiştir.  
  CNN modeli metindeki lokal kalıpları yakalarken; LSTM ve GRU zaman bağımlılıklarını modellemiştir.

- **Dropout ve Dense Katmanlar:**  
  Aşırı öğrenmeyi (overfitting) azaltmak için dropout katmanları eklenmiş, son katmanda dense katmanlar ile tahmin yapılmıştır.

- **Optimizasyon:**  
  Modeller `adam` optimizer ve `binary_crossentropy` kayıp fonksiyonu ile eğitilmiş, doğruluk metriği kullanılarak takip edilmiştir.

---

## 🚀 Kurulum

Proje klasörünü klonlayın:

```bash
git clone https://github.com/oguzhnsglm/Text_Sentiment_Analysis.git
cd Text_Sentiment_Analysis
```

Gerekli paketleri yükleyin:

```bash
pip install numpy pandas tensorflow matplotlib seaborn nltk
```

> Eğer Jupyter Lab/Notebook yoksa:
```bash
pip install notebook
```

---

## 📊 Çalıştırma

1️⃣ **Veri Temizleme ve Hazırlama:**

- `prepare_amazon.ipynb`
- `prepare_imdb.ipynb`
- `prepare_sentiment140.ipynb`

notebook dosyalarını açıp adım adım çalıştırarak veri ön işlemesini gerçekleştirin.

2️⃣ **Model Eğitimi ve Tahmin:**

- Notebook içinde CNN / LSTM / GRU modellerini eğitip `.keras` dosyalarını kaydedin veya hazır modelleri yükleyerek tahmin yapabilirsiniz.

---


## 📜 Lisans

MIT License
