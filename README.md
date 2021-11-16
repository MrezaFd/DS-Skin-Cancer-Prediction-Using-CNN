# Tugas-Besar-ML-059-055-

Data yang digunakan adalah data tentang kanker kulit ganas vs kanker kulit jinak

# 1. Download Data
Data yang digunakan berupa data yang sudah ada dari kaggle, setelah mendownload data dari kaggle menggunakan API token, lalu dilakukan extra dan pengecekan jumlah data yang terdapat dalam dataset

# 2. Prepocessing
Pada bagian prepocessing data dilakukan mainpulasi gambar menggunakan beberapa fungsi dari library OpenCV seperti membaca gambar(cv2,imread) dan mengubah ukuran gambar(cv2.resize). Setelah melakukan manipulasi gambar, proses selanjutnya adalah mengubah data menjadi array, lalu dilakukan pengecekan terhadap shapenya. Setelah itu melakukan normalisasi data, normalisasi data yang dilakukan adalah mengubah tipe data menjadi float agar bisa di train. Sebelum melakukan train data, data harus melalui proses penerapan label encoder yaitu merubah label data menjadi 0 dan 1

# 3. Modeling
Model yang dibuat menggunakan tensorflow.kers dengan menggunakan 1 input layer, 1 hidden layer dan 1 output layer. setelah input layer, dilakukan proses mengubah matriks 150x150x3 menjadi vektor sebelum masuk ke bagian hidden layer, pada hidden layer fungsi activation yang digunakan adalah 'relu' dan pada output layer funsgi yang digunakan adalah 'softmax'. Setelah membuat model, maka proses selanjutnya adalah training model yang sudah dibuat menggunakan optimizer Adam dengan learning rate = 0.0001, dengan batch size 32, dan iterasi sebanyak 60x.

# 4. Evaluasi Model
Pada bagian ini, dilakukan evaluasi terhadap model yang sudah ditraining sebelumnya menggunakan visualisasi grafik ggplot terhadap tingkat accuracy dan tingkat loss. selain menggunakan visualisasi hasil training, dilakukan juga evaluasi menggunakan classification_report untuk mengetahui tingkat accuracy dengan lebih pasti.
