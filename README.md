# DeepLearning-CNN
CNN (Convolutional Neural Network) adalah algoritma turunan dari neural network yang bekerja lebih khusus pada data citra digital (Image Recognition and Detection), Video, sinyal 1D (seperti suara, EKG) dan teks berurutan namun faktanya data lain misalnya log perangkat jaringan seperti pada dataset NSL-KDD dapat diproses namun tingkat akurasinya kalah dengan algoritma klasik seperti Random Forest dan Decision Tree, hal ini disebabkan data tersebut adalah data Tabular yaitu setiap fitur berdiri sendiri, tidak ada makna urutan antar fitur atau tidak ada pola yang bisa ditangkap oleh CNN, silahkan lihat detail hasil penelitian pada https://github.com/a9malik/Analisis-Perbandingan-Kinerja-CNN-DT-RF-Untuk-Deteksi-Intrusi-Jaringan-Pada-Dataset-NSL-KDD  

Perkembangannya adalah ANN (1980an) - CNN (1989) - Beyond CNN (2015-Now)

**Arsitektur CNN**
1. Input layer : Menerima gambar sebagai input dalam bentuk matriks (misalnya 224×224×3 untuk gambar RGB).
2. Convolutional Layer :
   - Conv1D : Untuk data sekuensial, seperti sinyal atau teks 
   - Conv2D : Untuk data 2D seperti gambar
   - Conv3D : Untuk data 3D Video atau citra volumetrik
4. Activation Layer : Membantu model belajar hubungan kompleks
5. Pooling Layer : Mengurangi dimensi lebar dan tinggi
6. Fully Connected Layer : Menggabungkan semua fitur yang di ekstrasi untuk menghasilkan prediksi akhir
7. Output Layer : Lapisan terakhir

**Perbedaan Convolutional Layer**

Conv1D  

![image](https://github.com/user-attachments/assets/e1c9a469-a336-4bbd-a674-09568140eb5b)


**Tahapan Penggunaan CNN**
1. Persiapan Data
   - Load dataset (contoh: pandas.read_csv).
   - Pra-pemrosesan data:
     - Normalisasi/skaling (contoh: StandardScaler dari scikit-learn).
     - Konversi label jika perlu (contoh: LabelEncoder).
     - Reshape data: jika CNN 1D → X.reshape(samples, features, 1)

2. Pelatihan Model
   - from tensorflow.keras.models import Sequential
   - from tensorflow.keras.layers import Conv2D, MaxPooling2D, Flatten, Dense, Dropout
   - model = Sequential([Conv2D(32, (3,3), activation='relu', input_shape=(32,32,3)),
     - MaxPooling2D(2,2),
     - Conv2D(64, (3,3), activation='relu'),
     - MaxPooling2D(2,2),
     - Flatten(),
     - Dense(128, activation='relu'),
     - Dropout(0.5),
     - Dense(10, activation='softmax')])
   - model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
   - model.fit(X_train, y_train, epochs=10, validation_data=(X_test, y_test))

3. Evaluasi dan Visualisasi
   - loss, acc = model.evaluate(X_test, y_test)
   - print(f"Akurasi: {acc:.4f}")


