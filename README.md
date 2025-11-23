PDF AI Query – Yapay Zekâ Destekli PDF Sorgulama Sistemi

Bu proje, kullanıcıların PDF dosyalarını yapay zekâ ile sorgulamasını sağlayan tamamen ücretsiz, lokalde çalışan bir uygulamadır.
Sistem, PDF’i okuyup anlamlı parçalara böler, embedding (vektör) çıkarır ve kullanıcının sorduğu soruya en alakalı metni PDF içinden bulup getirir.

🚀 Özellikler

✔ Tamamen ücretsiz

✔ Local çalışır (internet gerektirmez)

✔ PDF’i okuyup embed eden AI altyapısı

✔ Flask ile oluşturulmuş web arayüzü

✔ Soru–cevap formatında kullanım

✔ Birçok PDF ile çalışabilir (geliştirilebilir)

✔ Sentence Transformers modeli (all-MiniLM-L6-v2)

✔ PDF içinden en anlamlı parçayı bulup getirir

llm/
│── app.py               # Web sunucusu
│── embed.py             # PDF embedding işlemi
│── query.py             # Soru arama motoru
│── index.json           # Embedding veritabanı
│── example.pdf          # İşlenen PDF
│── requirements.txt     # Bağımlılıklar
│── templates/
│      └── index.html    # Web arayüzü

🔧 Kurulum
1) Gerekli paketleri yükle
pip install -r requirements.txt

2) PDF’i işlemek için embedding oluştur
python embed.py


Bu komut, PDF’i okuyup index.json dosyasını oluşturur.

3) Web sunucusunu başlat
python app.py

4) Tarayıcıdan uygulamayı aç
http://127.0.0.1:5000

💡 Kullanım

PDF dosyanı llm klasörüne yerleştir.

embed.py çalıştır → PDF için embedding oluşturur.

Web arayüzünde istediğin soruyu sor:

"Bu PDF'in konusu nedir?"

"Özet çıkar."

"X bölümünde ne anlatılıyor?"

Sistem PDF’den en uygun metni bulup ekrana getirir.

🤖 Kullanılan Yapay Zekâ Teknolojisi

Bu projede aşağıdaki ücretsiz AI teknolojileri kullanıldı:

Sentence Transformers → Embedding modeli

Model: all-MiniLM-L6-v2

Cosine Similarity → Sorgu ile PDF benzerliğini hesaplar

FAISS veya NumPy → Vektör karşılaştırma altyapısı

PyPDF2 → PDF okuma

Flask → Web arayüzü

🛠 Geliştirme Önerileri

🟦 Çoklu PDF desteği

🟩 Özetleme (local text generation modeli ile)

🟧 ChatPDF tarzı sohbet ekranı

🟪 Upload PDF özelliği

🟥 Semantic search geliştirme
