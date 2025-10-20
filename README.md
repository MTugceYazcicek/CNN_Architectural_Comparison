# CNN_Architectural_Comparison
## CNN Mimarilerinin CIFAR-10 Veri Seti Üzerinde Karşılaştırılması

Bu proje, CIFAR-10 veri seti üzerinde dört farklı Evrişimli Sinir Ağı (CNN) mimarisinin performansını karşılaştırmaktadır. Proje, `Cifar10_CNN.ipynb` Jupyter Notebook dosyası içerisinde detaylı olarak incelenmiştir.

## 🚀 Amaç

Projenin temel amacı, modern ve basit CNN mimarilerinin CIFAR-10 gibi standart bir görüntü sınıflandırma problemi üzerindeki başarımlarını, eğitim süreçlerini ve "overfitting" (aşırı öğrenme) eğilimlerini analiz etmektir.

## 🏛️ Karşılaştırılan Mimariler

Not defterinde aşağıdaki dört mimari eğitilmiş ve karşılaştırılmıştır:

1.  **Basit CNN:** Temel konvolüsyonel katmanlardan oluşan bir model.
2.  **NiN (Network in Network):** Geleneksel konvolüsyonel katmanlar yerine mikro sinir ağları kullanan bir yapı.
3.  **VGG-16:** Derin öğrenmede bir kilometre taşı olan, 16 katmanlı derin bir mimari.
4.  **ResNet-50:** "Residual" (artık) bağlantıları kullanarak çok derin ağların eğitilmesini sağlayan modern bir mimari.

## 📊 Temel Bulgular

Not defterindeki analizlere göre elde edilen temel sonuçlar:

* **VGG-16:** En yüksek test doğruluğunu ve en dengeli performansı gösteren model olmuştur. Eğitim ve test arasında kabul edilebilir bir farkla (hafif overfitting) en başarılı sonucu vermiştir.
* **ResNet-50:** Eğitim verisini ezberleyerek (eğitim başarımı çok yüksek) test verisinde çok düşük bir başarım göstermiştir. Açık bir "overfitting" durumu gözlemlenmiştir.
* **NiN:** Eğitim ve test başarımları birbirine çok yakın, overfitting eğilimi göstermeyen stabil bir modeldir. Başarısı orta düzeydedir.
* **Basit CNN:** VGG-16'ya benzer şekilde, hafif overfitting eğilimi gösteren ancak kabul edilebilir ve dengeli bir performans sunmuştur.

## 🛠️ Kurulum ve Kullanım

Projeyi yerel makinenizde veya Google Colab üzerinde çalıştırabilirsiniz.

### Gereksinimler

Projenin çalışması için gerekli olan Python kütüphaneleri `requirements.txt` dosyasında listelenmiştir.

### Yerel Kurulum

1.  Depoyu klonlayın:
    ```bash
    git clone [https://github.com/MTugceYazcicek/CNN_Architectural_Comparison.git](https://github.com/MTugceYazcicek/CNN_Architectural_Comparison.git)
    cd CNN_Architectural_Comparison
    ```

2.  (Önerilir) Bir sanal ortam (virtual environment) oluşturun ve aktifleştirin:
    ```bash
    python -m venv venv
    source venv/bin/activate  # Windows için: venv\Scripts\activate
    ```

3.  Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install -r requirements.txt
    ```

4.  Jupyter Notebook'u başlatın:
    ```bash
    jupyter notebook Cifar10_CNN.ipynb.ipynb
    ```
---

## Acknowledgements (Teşekkür ve Atıf)

Bu projede kullanılan CIFAR-10 veri seti, Alex Krizhevsky, Vinod Nair ve Geoffrey Hinton tarafından sağlanmıştır.

Veri seti hakkında daha fazla bilgi ve resmi atıf için:
* [CIFAR-10 Dataset Page (Toronto Üniversitesi)](https://www.cs.toronto.edu/~kriz/cifar.html)
* **Resmi Atıf:** *Alex Krizhevsky, "Learning Multiple Layers of Features from Tiny Images", 2009.* (Teknik Rapor)
