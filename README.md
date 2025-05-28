## E-Posta Spam Tespiti (Spam vs. Ham)

Bu proje, bir e-posta mesajının **"Spam"** (istenmeyen) mi yoksa **"Ham"** (normal) mi olduğunu tahmin etmek için **Makine Öğrenmesi** kullanır. Kullanıcıdan alınan e-posta içeriği analiz edilir ve mesajın kategorisi belirlenir.

---

##  Kullanılan Teknolojiler

- Python 3.x
- scikit-learn
- pandas
- TfidfVectorizer
- Naive Bayes (MultinomialNB)
- Jupyter Notebook veya Visual Studio Code

---

##  Veri Kümesi

Proje, [UCI SMS Spam Collection Dataset](https://archive.ics.uci.edu/ml/datasets/sms+spam+collection) adlı veri setini kullanır.

CSV dosyasının adı: `spam.csv`  
Kullanılan sütunlar:
- `v1`: Etiket (spam / ham)
- `v2`: E-posta veya SMS mesajı

---

##  Nasıl Çalışır?

1. **Veri Yükleme**: `spam.csv` dosyası okunur.
2. **Temizlik & Hazırlık**: Sadece mesaj ve etiket sütunları alınır.
3. **TF-IDF Vektörleme**: Metinler sayısal değerlere dönüştürülür.
4. **Veri Bölme**: Eğitim ve test için ayrılır.
5. **Model Eğitimi**: Naive Bayes algoritması kullanılır.
6. **Tahmin**: Model, test verisinde ne kadar başarılı test edilir.
7. **Kullanıcıdan Girdi**: Kullanıcıdan e-posta alınır ve sınıflandırılır.

---

##  Kullanılan Algoritma

**Naive Bayes Classifier**:  
Metin verilerinde oldukça etkili olan bu algoritma, özellikle "kelime olasılıklarına" göre sınıflandırma yapar. Burada `MultinomialNB` modeli kullanılmıştır.

---

##  Performans

Model aşağıdaki metriklerle değerlendirilmiştir:

- **Accuracy (Doğruluk)**: %96
- **Precision / Recall / F1-Score**: `classification_report` çıktısında gösterilmiştir.

---

##  Kurulum

1. Bu projeyi klonlayın:
```bash
git clone https://github.com/muhametaliaslanhan/E-Posta-Spam-mi-Ham-mi.git
cd E-Posta-Spam-mi-Ham-mi
```

#  Gerekli kütüphaneleri indirin.
```bash
pip install pandas scikit-learn
```
## Kullanım

# Jupyter notebook veya Visual Studio ile kodu çalıştırın.
1.Jupyter notebook için terminale yazın👇.
```bash
jupyter notebook
```
2. kodu çalıştırın ve örnek E-Postanızı input olarak girin ve sonucu görün.
3. Eğer elininde örnek E-Posta yok ise örnek E-posta örneklerinden hazır sınıflandırılmış örnekleri input olarak girebilirsiniz.
```bash
E-Posta-Spam-mi-Ham-mı
├──.gitattributes
├──.gitignore
├──spam.csv
├──spammi hammi_son.ipynb
├──örnek eposta.txt
```










