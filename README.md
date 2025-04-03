# Flask Quiz Uygulaması

Bu proje, Flask kullanılarak geliştirilmiş, SQLite veritabanı ile entegre edilmiş interaktif bir quiz uygulamasıdır.

## Özellikler

- İnteraktif sorular ve çoktan seçmeli cevaplar
- Kullanıcı skoru takibi
- Kişisel en yüksek skor takibi
- Genel yüksek skor sıralaması
- Duyarlı tasarım (responsive design)

## Proje Yapısı

```
FlaskQuizPy/
├── app/                    # Ana uygulama paketi
│   ├── models/             # Veritabanı modelleri
│   │   ├── __init__.py
│   │   └── quiz.py         # Soru ve UserScore modelleri
│   ├── static/             # Statik dosyalar
│   │   ├── css/            # CSS stilleri
│   │   └── js/             # JavaScript dosyaları
│   ├── templates/          # HTML şablonları
│   │   ├── base.html       # Ana şablon
│   │   ├── index.html      # Ana sayfa
│   │   ├── start_quiz.html # Quiz başlatma
│   │   ├── question.html   # Soru sayfası
│   │   ├── quiz_result.html # Sonuç sayfası
│   │   └── high_scores.html # Yüksek skorlar
│   ├── views/              # Görünüm fonksiyonları
│   │   ├── __init__.py
│   │   └── main.py         # Ana rotalar
│   └── __init__.py         # Uygulama fabrikası
├── instance/               # Veritabanı dosyası (quiz.db)
├── README.md               # Bu doküman
├── requirements.txt        # Bağımlılıklar
├── run.py                  # Uygulamayı çalıştırma
└── seed_db.py              # Veritabanını örnek verilerle doldurma
```

## Kurulum

### Gereksinimler

- Python 3.8 veya daha yeni

### Adımlar

1. Projeyi indirin:
   ```bash
   git clone https://github.com/asimbaki/FlaskQuizPy.git
   cd FlaskQuizPy
   ```

2. Sanal ortam oluşturun ve aktif edin:
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # Linux/Mac
   source venv/bin/activate
   ```

3. Bağımlılıkları yükleyin:
   ```bash
   pip install -r requirements.txt
   ```

4. Veritabanını örnek sorularla doldurun:
   ```bash
   python seed_db.py
   ```

5. Uygulamayı çalıştırın:
   ```bash
   python run.py
   ```

6. Tarayıcınızda `http://127.0.0.1:5000` adresine giderek uygulamayı kullanmaya başlayın.

## Teknoloji Yığını

- [Flask](https://flask.palletsprojects.com/) - Web çatısı
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/) - ORM
- [Bootstrap](https://getbootstrap.com/) - Arayüz tasarımı
- [SQLite](https://www.sqlite.org/) - Veritabanı

## Kullanım

1. Ana sayfadan "Quiz'e Başla" butonuna tıklayın
2. Kullanıcı adınızı girin
3. Her soruyu cevaplayın (A, B, C veya D seçeneklerinden birini seçin)
4. Quiz tamamlandığında sonuçlarınızı görün
5. İsterseniz "Tekrar Oyna" butonuna tıklayarak yeni bir quiz başlatın
6. "Yüksek Skorlar" kısmından en iyi skorları görüntüleyin

