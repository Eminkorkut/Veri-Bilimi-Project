# Veri Bilimi Projesi: BT Görüntülerinden COVID-19 Tespiti

Bu repo, SARS‑CoV‑2 CT-scan veri seti kullanılarak BT (Bilgisayarlı Tomografi) görüntülerinden otomatik COVID‑19 tespiti için derin öğrenme tabanlı sınıflandırma çalışmalarını içerir. Çalışmada farklı mimariler (özel CNN, ResNet18 ve Vision Transformer) aynı veri seti üzerinde karşılaştırılır; doğruluk, kesinlik, duyarlılık, F1-skoru gibi metriklerle değerlendirme yapılır.

## İçerik

- `main.ipynb`: Eğitim/validasyon/test akışı, model tanımları ve metrik hesaplamaları.
- `conference_101719.tex`: IEEE konferans formatında rapor/makale kaynağı.
- `IEEEtran.cls`: LaTeX sınıf dosyası.
- `Veri_Bilimi_Projesi.pdf`: Üretilmiş rapor/çıktı PDF’i.

## Veri Seti

Notebook, Kaggle üzerinde bulunan **SARS‑CoV‑2 CT-scan** veri seti dizinini varsayılan olarak aşağıdaki şekilde kullanır:

- `data_path = "/kaggle/input/sarscov2-ctscan-dataset"`

Yerel çalıştıracaksanız bu yolu, veri setinin bilgisayarınızdaki konumuna göre güncelleyin.

## Kurulum

Notebook PyTorch ve ilgili ekosistemi kullanır. Temel bağımlılıklar:

- Python 3.x
- `torch`, `torchvision`
- `numpy`, `pandas`
- `matplotlib`, `seaborn`
- `scikit-learn`

Ortamınızı kurduktan sonra notebook’u Jupyter/VS Code ile açıp çalıştırabilirsiniz.

## Çalıştırma

1. `main.ipynb` içindeki `data_path` değişkenini ortamınıza göre ayarlayın.
2. GPU varsa otomatik olarak `cuda` kullanılacak şekilde yapılandırılmıştır.
3. Hücreleri sırayla çalıştırarak:
   - veri bölme (train/val/test),
   - model eğitimleri,
   - karmaşıklık matrisi / ROC gibi değerlendirmeleri elde edebilirsiniz.

## Rapor (LaTeX)

Makale kaynağı `conference_101719.tex` dosyasındadır. PDF çıktısı repoda `Veri_Bilimi_Projesi.pdf` olarak bulunur.

## Lisans / Not

Bu çalışma eğitim/akademik amaçlıdır. Veri setinin lisans ve kullanım koşulları için lütfen veri setinin yayınlandığı sayfadaki şartları inceleyin.

