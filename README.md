# heart_disease_classification
project yang memiliki tujuan untuk mengklasifikasikan teks berupa keluhan pelanggan berdasarkan identifikasi penyakit jantung menurut teks tersebut

cara penggunaan model:
1. install transformer
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/3dbeef05-3e94-4d90-bc60-966aceadd7dd)
   run cell diatas

2. preprocess
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/5fec015e-0c89-47bc-a192-2461204a6e0a)
   sebelum run code diatas, upload terlebih dahulu file "cleaned_shuffled_dataset.csv", yang tersedia di github, ke google colab. file tersebut merupakan dataset dari model ini.

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/a8e09474-734d-454b-969a-93631873d7d4)
   run cell diatas. cell ini untuk mengimpor tokenizer

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/e84c8efe-49c0-48d0-a937-bf0bb83c0ca3)
   run kedua cell diatas diatas. cell ini untuk mengatur format nama dari dataset

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/c58dc7b2-51b0-45af-942f-fdb6ba43e991)
   run kedua cell diatas. cell ini untuk melakukan tokenization pada train set dan test set serta mengimpor padding

3. evaluate
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/4b83237f-6b8a-4820-843e-328e3e10f1aa)
   run kedua cell diatas. cell ini untuk mengimpor dan mengatur evaluasi model nantinya

4. train
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/3ebe3e31-fe55-486c-89e0-b001d3f2930f)
   run kedua cell diatas. cell ini untuk mengimpor model yang sudah pernah di train sebelumnya, namun kali ini kita tetap melakukan train ulang sesuai dengan dataset yang dimiliki

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/98cbf223-7042-4089-89b1-c93586450888)
   run cell diatas. cell ini untuk menentukan nilai hyperparamaters serta konfigurasi model dan mengeksekusi training

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/ec7ad6e2-10af-44f8-9207-8365aaa0d4b3)
   terdapat bagian [344/344 09:02, Epoch 8/8] pada gambar diatas yang merupakan salah satu keterangan hasil training yang baru saja dilakukan. 344 yang tertera pada segmen keterangan hasil training tersebut     
   merupakan letak folder model hasil training beserta file konfigurasinya. berikut adalah gambar lebih tepatnya dari letak folder model hasil training tersebut.
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/3c61ced9-718b-41ae-95c7-f33fd3efab65)


5. inference
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/82e2ac5a-0bf7-492e-accf-a42b00827ce8)
   sebelum run cell diatas, ganti kolom input segmen code "tokenizer = AutoTokenizer.from_pretrained("/content/seq_model/checkpoint-344")" dan "model =   
   AutoModelForSequenceClassification.from_pretrained("/content/seq_model/checkpoint-344")" dengan nomor penanda letak folder model hasil train, yang dimana pada contoh ini adalah 344. jadi jika nomornya adalah 
   155, maka segmen code menjadi "tokenizer = AutoTokenizer.from_pretrained("/content/seq_model/checkpoint-155")" dan "model = AutoModelForSequenceClassification.from_pretrained("/content/seq_model/checkpoint- 
   155")". namun, jika nomornya tetap 344, maka tidak perlu diubah.

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/fa80d648-5016-46b7-ad20-c66eef261dd5)
   sebelum run cell diatas, upload terlebih dahulu file test set untuk model ini yang tersedia juga pada github, yaitu "test_dataset1.csv" ke google colab.

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/dc03f516-f541-44e1-b80f-32556503ca34)
   run cell diatas. cell ini untuk mengklasifikasikan test data menggunakan model yang sudah di train

   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/0c6fba27-8068-416a-ae3b-edddcdb54ef4)
   untuk keperluan testing model menggunakan data sendiri secara manual, pakai saja cell diatas. ganti segmen code yang ada di dalam petik dua berdasarkan gambar dibawah dengan text yang mengandung keluhan pasien.
   ![image](https://github.com/ayubstak/heart_disease_classification/assets/92737338/0cd59329-8c8e-4ec4-92e9-234dcd974fd6)
   lalu run cell nya. jika hasilnya adalah "YES", maka text tersebut diklasifikasikan merupakan keluhan dari pasien yang terkena penyakit jantung. jika "NO", maka tidak terkena penyakit jantung.

   
   











