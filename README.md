# Covid-19 Hasta Verisi Analizi

Bu proje, gerçek hasta verileri üzerinde temel veri analizi yaparak Covid-19'un ölüm oranları ve risk faktörlerini incelemektedir.

## İçerik

- Veri setinin yüklenmesi ve temizlenmesi
- Yaş gruplarına göre ölüm oranı analizi
- Cinsiyete göre ölüm oranı analizi
- Entübe olan hastaların ölüm oranı
- Diyabet, KOAH, astım ve zatürre gibi hastalıkların ölüm oranına etkisi
- Verilerin görselleştirilmesi (grafikler ile destekli)

## Kullanılan Kütüphaneler

- pandas
- numpy
- matplotlib
- seaborn

## Proje Akışı

1. **Veri Yükleme**  
   Covid-19 hasta verileri `.csv` formatında yüklenerek `pandas` DataFrame'e aktarılmıştır.

2. **Veri Temizleme**  
   - 98 ve 99 gibi eksik/yanlış değerler `NaN` olarak düzeltilmiştir.
   - `IS_DEAD` isimli yeni bir kolon oluşturulmuştur (`ÖLÜM_TARİHİ` bilgisine göre).

3. **Ölüm Oranı Analizleri**  
   - Yaş gruplarına (0-10, 10-20, ..., 90-100) göre ölüm oranı hesaplanmıştır.
   - Cinsiyetlere göre ölüm oranı karşılaştırılmıştır.
   - Entübe edilen hastalar için ölüm oranı analiz edilmiştir.
   - Diyabet, KOAH, astım ve zatürre hastalığı taşıyan hastaların ölüm oranı incelenmiştir.

4. **Veri Görselleştirme**  
   - Ölüm oranları çubuk grafikleri ile gösterilmiştir.
   - Hastalık durumlarına göre ölüm oranı tablolar ve grafiklerle desteklenmiştir.

## Nasıl Çalıştırılır?

1. Projeyi bilgisayarınıza klonlayın:

    ```bash
    git clone https://github.com/kullanici-adi/Covid19AnalizProjesi.git
    cd Covid19AnalizProjesi
    ```

2. Gerekli kütüphaneleri kurun:

    ```bash
    pip install pandas numpy matplotlib seaborn
    ```

3. Jupyter Notebook üzerinden çalıştırın:

    ```bash
    jupyter notebook Covid19AnalizProjesi.ipynb
    ```

## Notlar

- Veri setindeki 98 ve 99 gibi değerler eksik veri olarak (`NaN`) kabul edilmiştir.
- Ölüm oranı hesaplamalarında yalnızca geçerli (eksiksiz) veriler kullanılmıştır.
- Projede görselleştirme için **Matplotlib** ve **Seaborn** kütüphaneleri kullanılmıştır.

## Lisans

Bu proje eğitim amaçlı hazırlanmıştır. Veri setine ilişkin tüm haklar ilgili sağlık kurumlarına aittir.

## Veri Kaynağı

Bu projede kullanılan veri seti, Kaggle platformundan alınmıştır:  
[Covid-19 Dataset by Meir Nizri](https://www.kaggle.com/datasets/meirnizri/covid19-dataset)

