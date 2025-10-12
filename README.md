# 🌿 Klasifikasi Rempah-Rempah Menggunakan CNN (MobileNetV2)

Proyek ini menerapkan metode **Deep Learning** berbasis **Convolutional Neural Network (CNN)** dengan model **MobileNetV2** untuk mengklasifikasikan berbagai jenis rempah-rempah. Model dikembangkan menggunakan **Python** dan **TensorFlow Keras** dengan pendekatan **Transfer Learning** untuk meningkatkan efisiensi dan akurasi pada dataset terbatas.

---

## 📖 Deskripsi

Klasifikasi citra rempah-rempah merupakan salah satu penerapan visi komputer yang bertujuan untuk mengidentifikasi jenis rempah berdasarkan karakteristik visualnya. Dalam proyek ini, digunakan model **MobileNetV2**, salah satu arsitektur CNN ringan yang efisien dan memiliki performa tinggi untuk klasifikasi gambar.

Dengan memanfaatkan **augmentasi data** dan **transfer learning**, model ini mampu belajar dari dataset rempah dengan jumlah terbatas dan memberikan hasil klasifikasi yang akurat tanpa memerlukan pelatihan dari awal (scratch).

---

## 🧩 Arsitektur Model

Model dikembangkan dengan pendekatan **fine-tuning MobileNetV2**, dengan arsitektur sebagai berikut:

- **Base model**: MobileNetV2 (pre-trained pada ImageNet, tanpa top layer)
- **Global Average Pooling Layer**
- **Dense Layer**: 128 neuron, aktivasi ReLU
- **Dropout Layer**: 0.3
- **Output Layer**: Softmax sesuai jumlah kelas (`num_classes`)

Model dikompilasi menggunakan:
- **Optimizer**: Adam (learning rate 0.0001)
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy

---

## 🧰 Teknologi yang Digunakan

- Python 3  
- TensorFlow / Keras  
- Matplotlib  
- NumPy  
- Google Colab  

---

## 📊 Data dan Augmentasi

Dataset: `rempah_dataset`  
Dataset dibagi menjadi **80% data latih** dan **20% data validasi**.  
Augmentasi dilakukan dengan:
- `rotation_range=25`  
- `width_shift_range=0.2`  
- `height_shift_range=0.2`  
- `shear_range=0.2`  
- `zoom_range=0.3`  
- `horizontal_flip=True`  

---

## 🚀 Callback yang Digunakan

Model menggunakan beberapa callback penting:
- **EarlyStopping** → menghentikan training saat akurasi tidak meningkat  
- **ReduceLROnPlateau** → menurunkan learning rate otomatis  
- **ModelCheckpoint** → menyimpan model terbaik selama training  

---

## 📈 Hasil dan Evaluasi

Model menunjukkan performa yang baik pada dataset rempah-rempah dengan tingkat akurasi tinggi pada data validasi.  
(“Akurasi validasi: 89.47%”).  

Visualisasi training dan validasi divisualisasikan menggunakan **Matplotlib** untuk menampilkan kurva *accuracy* dan *loss*.

---


---

## 📚 Kesimpulan

Model **MobileNetV2** berhasil mengklasifikasikan berbagai jenis rempah-rempah secara efisien dan akurat dengan memanfaatkan transfer learning.  
Pendekatan ini menunjukkan bahwa CNN ringan seperti MobileNetV2 cocok untuk aplikasi klasifikasi citra dalam skala kecil hingga menengah.

---

## 👨‍💻 Pengembang

Dikembangkan oleh: ** AHMAD RIKHAN ARBAI **  
Sebagai bagian dari pembelajaran dan penerapan metode **Deep Learning CNN menggunakan Keras**.
