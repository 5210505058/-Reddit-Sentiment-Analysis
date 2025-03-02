# Reddit Sentiment Analysis

Bu proje, Reddit'in `investing` subreddit'inden alınan gönderiler üzerinde duygu analizi (sentiment analysis) yapar ve sonuçları görselleştirir. Python ve çeşitli kütüphaneler kullanılarak geliştirilmiştir.

## Kullanılan Kütüphaneler
- `praw`: Reddit API'sine bağlanmak ve veri çekmek için kullanılır.
- `pandas`: Verileri işlemek ve analiz etmek için kullanılır.
- `matplotlib`: Verileri görselleştirmek için kullanılır.
- `wordcloud`: Metin verilerinden kelime bulutu oluşturmak için kullanılır.
- `vaderSentiment`: Metinlerin duygu skorlarını hesaplamak için kullanılır.

## Kurulum

### Gereksinimlerin Yüklenmesi
Projeyi çalıştırmak için gerekli kütüphaneleri yükleyin:

```bash
pip install praw pandas matplotlib wordcloud vaderSentiment
```

### Reddit API Bilgileri
Reddit API'sine bağlanmak için kendi `client_id`, `client_secret` ve `user_agent` bilgilerinizi kullanın. Bu bilgileri `praw.Reddit` fonksiyonuna girin:

```python
import praw

reddit = praw.Reddit(
    client_id="YOUR_CLIENT_ID",
    client_secret="YOUR_CLIENT_SECRET",
    user_agent="YOUR_USER_AGENT"
)
```

Reddit API anahtarlarını almak için [Reddit Apps](https://www.reddit.com/prefs/apps) sayfasına giderek yeni bir uygulama oluşturabilirsiniz.

## Projenin Çalıştırılması
Projeyi çalıştırmak için aşağıdaki komutu kullanın:

```bash
python reddit_sentiment_analysis.py
```

Bu komut, Reddit'ten verileri çekecek, duygu analizi yapacak ve sonuçları görselleştirecektir. Ayrıca, analiz sonuçlarını bir CSV dosyası olarak kaydedecektir.

## Çıktılar

### Pasta Grafiği (Pie Chart)
Gönderilerin duygu dağılımını gösteren bir pasta grafiği oluşturulur. Grafik, pozitif, negatif ve nötr duyguların yüzdelik dağılımını gösterir.
![pie](https://github.com/user-attachments/assets/15f85b8a-3d9f-4f41-8931-2703f8d862e8)


### Kelime Bulutu (Word Cloud)
Gönderilerde en sık kullanılan kelimeleri gösteren bir kelime bulutu oluşturulur.
![year](https://github.com/user-attachments/assets/ca1c67cf-082e-4a92-8a7e-855df78750ce)


### CSV Dosyası
Analiz sonuçları `reddit_sentiment_analysis.csv` adlı bir CSV dosyasına kaydedilir. Bu dosya, her gönderinin metnini ve duygu skorlarını içerir.


## Lisans
Bu proje **MIT lisansı** altında lisanslanmıştır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasına bakabilirsiniz.

> **Not:** Bu proje eğitim amaçlı olarak geliştirilmiştir. Reddit API'sini kullanırken, Reddit'in kullanım koşullarına ve kurallarına uygun davranmayı unutmayın.


