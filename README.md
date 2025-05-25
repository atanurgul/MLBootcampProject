# MLBootcampProject

Wine Quality Prediction

Projenin Amacı
Bu projede, kırmızı şarapların içerdiği kimyasal özelliklere bakarak şarabın kalitesini tahmin etmeyi amaçladım. Kalite skorlarını üç sınıfa ayırarak (düşük, orta, yüksek) daha kapsamlı bir sınıflandırma problemi oluşturdum.

Kullanılan Veri Seti
- Kaynak: [UCI - Wine Quality Data Set](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- Veride sabit asitlik, uçucu asitlik, alkol oranı gibi birçok kimyasal ölçüm bulunuyor bu yüzden çok güzel bir veri seti.
- Orijinal kalite skoru 0-10 arası. Biz bu skoru daha iyi ve ayrıntılı olması için kategorilere ayırdım:
  - 0-4: Düşük
  - 5-6: Orta
  - 7-10: Yüksek

Adım adım nasıl yaptım
- Öncelikle veriyi düzenledim ve kalite skorunu sınıflara ayırdım.
- Etiketleme için `LabelEncoder` kullandım.
- Sınıflar arasında dengesizlik vardı ve bunu `SMOTE` yöntemiyle dengeledim.
- Model olarak `RandomForestClassifier` seçtim çünkü çok sınıflı ve karmaşık verilerde çok daha iyi sonuç veriyor.
- En iyi sonuçları almak için `GridSearchCV` ile hiperparametre optimizasyonu yaptım.

Sonuçlar
- Test verisi üzerinde tahmin yaptırdım ve `classification_report` ile modelin başarı durumunu ölçtüm.
- F1 Score, Precision ve Recall değerleri özellikle orta ve yüksek sınıflarda harika seviyedeydi.

Kaggle Notebook Linki
......
