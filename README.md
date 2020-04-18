# :fire: PyTorch ile Görüntü Sınıflandırma 

Bir süredir PyTorch üzerinden pratikler yapmaya çalışıyorum. Caffe ile başlayan yolculuğum, TensorFlow ve Keras ile güzel devam etti ama neden PyTorch'un da nimetlerini öğrenmeyeyim ki diye düşünüyorum. :sunglasses: Geçtiğimiz hafta içinde [People In Data](https://www.facebook.com/peopleindata/) ve [Facebook DevC Stockholm](https://www.facebook.com/groups/devCstockholm/) ortaklığıyla düzenlenen etkinlikte **Udacity AI** mentorlerinden _Pranjal_ ile tanışmış oldum ve harika bir webinar gerçekleştirdi. Tabi hem Pytorch'a ısınmam için hem de bu sırada meraklılarına faydalı olması adına bu notebook'u hazırlamaya karar verdim. Destek veren [Pranjal](https://www.linkedin.com/in/pranjall/?originalSubdomain=in)'a ve bu etkinlik hakkında beni haberdar ettiği için [Zümrüt](https://www.linkedin.com/in/zumrut-muftuoglu-98704537/)e teşekkürler.

Bu Colab Notebookda, Evrişimli Sinir Ağları temellerini kullanarak basit bir görüntü sınıflandırma çalışması uygularken [PyTorch Ekosistemindeki](https://pytorch.org/ecosystem/ "Click to visit the PyTorch Ecosystem homepage") yeniliklerden de faydalanacağız.

### Başlıklar Şöyle:
**1. Colab Üzerinde Veri Setini Veri Setlerini Kullanma**
**2. Eğitim, Doğrulama/Geçerleme ve Test Kümelerinin Oluşturulması**
**3. Dataloaderların Hazırlanması**
**4. PyTorch Kullanarak CNN Modeli Oluşturma**
   _4.1.1. Evrişimli Sinir Ağı (CNN) Mimarisi
   4.1.2 Temel bir CNN Katmanı
   4.1.3 Adım kaydırma (Stride)
   4.1.4 Piksel Ekleme (Padding)
   4.1.5 Maksimum Ortaklama (Max-Pooling)
   4.1.6 Aktivasyon Fonksiyonu: ReLU (Rectified Linear Units)
   4.1.7 Tam Bağlantılı, Lineer Bağlantılı Katmanlar (Fully Connected or Linear Layers)
   4.2.1 PyTorch (Gelelim Sadede)
   4.2.2 Hesaplamalı Grafikleri (Computational Graph) Anlama
   4.2.3 Tensörler
   4.2.4 Autograd Modülü
   4.2.5 nn.Module
   4.2.6 Optim Paketi
   4.3 Modelimizi tanımlama zamanı!_
**5. 2020'de bir PyTorch Modeli Eğitelim** 
**6. Aşırı Uydurma/Öğrenme (Ezberleme) ya da Overfitting naıl birşeydir anlayalım**   
**7. Daha İyi Bir Eğitim Döngüsü**
**8. Daha Alımlı Bir Eğitim Döngüsü**
**9. SONUÇ**
**10. Teşekkürler**

📌[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ayyucekizrak/) **Google Colab Not Defteri**


📌[![Open In Jupyter](https://github.com/jupyter/notebook/blob/master/docs/resources/icon_32x32.svg)](https://nbviewer.jupyter.org/github/ayyucekizrak/) **Jupyter Not Defteri** 


### Başlayalım!!! 
<img align="center" src="https://media.giphy.com/media/oio1NtBHjowYE/giphy.gif" width=40% />

---

_Gently Thanks to [Pranjal](https://www.linkedin.com/in/pranjall/?originalSubdomain=in) for awesome webinar and thanks to [Zümrüt](https://www.linkedin.com/in/zumrut-muftuoglu-98704537/) for invited me to the webinar_ 
<br/>Not:
https://github.com/pranjalchaubey/Deep-Learning-Notes
