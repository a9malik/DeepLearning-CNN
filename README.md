# DeepLearning-CNN
CNN (Convolutional Neural Network) adalah algoritma turunan dari neural network yang bekerja lebih khusus pada data citra digital (Image Recognition and Detection), Video, sinyal 1D (seperti suara, EKG) dan teks berurutan namun faktanya data lain misalnya log perangkat jaringan seperti pada dataset NSL-KDD dapat diproses namun tingkat akurasinya kalah dengan algoritma klasik seperti Random Forest dan Decision Tree, hal ini disebabkan data tersebut adalah data Tabular yaitu setiap fitur berdiri sendiri, tidak ada makna urutan antar fitur atau tidak ada pola yang bisa ditangkap oleh CNN, silahkan lihat detail hasil penelitian pada 
Perkembangannya adalah ANN (1980an) - CNN (1989) - Beyond CNN (2015-Now)

Arsitektur CNN : 
1. Input layer : Menerima gambar sebagai input dalam bentuk matriks (misalnya 224×224×3 untuk gambar RGB).
2. Convolutional Layer : Filter (misalnya 3x3 atau 5x5)
3. Activation Layer : Membantu model belajar hubungan kompleks
4. Pooling Layer : Mengurangi dimensi lebar dan tinggi
5. Fully Connected Layer : Menggabungkan semua fitur yang di ekstrasi untuk menghasilkan prediksi akhir
6. Output Layer : Lapisan terakhir
