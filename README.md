> **Materi:** *"Attributing Direct Drivers to Deforestation Alerts with Satellite Imagery and AI"*  
> **Narasumber:** Bart Slagter  
> **Penyelenggara:** Informatics Practitioner Lecture Series Program Studi Informatika, Universitas Bengkulu  
> **Tautan Video Webinar:** [YouTube Live - Informatics Practitioner Lecture Series](https://www.youtube.com/live/OFLzys5FYqg?si=MbfRr0vpfpg5O1hU)

---

## 📌 Ringkasan Studi Kasus

Sistem Peringatan Dini Satelit (**RADD / GLAD**) baru saja mendeteksi adanya indikasi hilangnya tutupan pohon seluas **20 hektar** di area Koridor Konservasi Hutan Gambut Lindung. Tim respon cepat penegakan hukum lingkungan membutuhkan identifikasi pemicu utama (*direct drivers*) secara otomatis dari data citra satelit sebelum menerjunkan personel ke lapangan.

### **Pertanyaan Bisnis & Operasional**
> *"Apa pemicu utama (direct driver) dari pembukaan lahan yang terdeteksi satelit, dan tindakan penanganan cepat apa yang harus diambil oleh tim lapangan?"*

### **Solusi Data Science & AI**
Menggunakan model **Deep Learning (Convolutional Neural Network - CNN)** untuk memproses masukan citra satelit multisensor (Sentinel-1 SAR & Sentinel-2 Optik), memprediksi kategori pemicu deforestasi secara otomatis, dan mengevaluasi ketepatannya menggunakan metrik **F1-Score**.

---

## 🔄 Metodologi Implementasi AI

Proyek ini dilaksanakan mengikuti 6 tahapan alur kerja *Deep Learning & Remote Sensing*:

```
[Problem Definition] ➡️ [Satellite Data Input] ➡️ [Data Preprocessing & Backfilling]
                                                                  ⬇️
[Field Action & Decision] ⬅️ [F1-Score Evaluation] ⬅️ [CNN Deep Learning Modeling]
```

1. **Problem Definition:** Identifikasi kebutuhan respon cepat antara tindakan mediasi sosial vs penegakan hukum tegas berdasarkan pemicu deforestasi.
2. **Satellite Data Input:** Menganalisis patch citra satelit multispektral (Red, Green, Blue, NIR dari Sentinel-2) dan radar (VV/VH dari Sentinel-1).
   > *Catatan:* Pada skrip koding Python di Google Colab, digunakan simulasi patch citra satelit sintetis multisensor berukuran 32x32 piksel yang merepresentasikan pola spasial-spektral kawasan hutan.
3. **Data Preprocessing & Backfilling:** Penerapan teknik *backfilling* (komposit citra bebas awan 1–6 bulan ke belakang) untuk mengatasi kendala tutupan awan tebal di hutan tropis.
4. **CNN Modeling:** Membangun arsitektur *Convolutional Neural Network* (Conv2D, MaxPooling, Dropout, Dense Layer) untuk mengklasifikasikan 4 kategori pemicu deforestasi.
5. **Evaluation:** Mengukur performa model menggunakan metrik **F1-Score (Macro)** untuk memastikan keandalan deteksi tiap kategori pemicu.
6. **Field Action & Decision:** Mengintegrasikan hasil prediksi model ke platform **Global Nature Watch** (`globalnaturewatch.org`) untuk pemetaan patroli presisi.

---

## 📈 4 Level Tingkatan Analytics

| Level Analytics | Pertanyaan Utama | Hasil / Implementasi pada Kasus |
| :--- | :--- | :--- |
| **Descriptive** | *Apa yang terjadi?* | Peringatan satelit mendeteksi 20 hektar tutupan pohon hilang di zona hutan lindung. |
| **Diagnostic** | *Mengapa ini terjadi?* | Analisis citra satelit menunjukkan adanya pola tekstur dan reflektansi spektral khas aktivitas manusia (pembuatan kanal/jalan, pembakaran, atau tebang liar). |
| **Predictive** | *Apa yang akan terjadi?* | Model CNN memprediksi kategori *Direct Driver* pembukaan lahan secara otomatis dari masukan patch citra satelit. |
| **Prescriptive** | *Apa tindakan terbaik?* | Menentukan skema intervensi lapangan: Penegakan hukum tegas untuk *Canal/Road Clearing* & *Selective Logging*, atau mediasi sosial untuk *Smallholder Encroachment*. |

---

## 📊 Ringkasan Hasil Model & Evaluasi

| Model Deep Learning | Accuracy | Precision | Recall | Overall Macro F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Convolutional Neural Network (CNN)** | **100%** | **1.00** | **1.00** | **1.0000** |

### **Rincian Klasifikasi Pemicu Deforestasi (Direct Drivers):**
1. **`Selective Logging`**: Penyiapan tim penegakan hukum dan penyitaan jalur keluar kayu.
2. **`Fire Clearing`**: Mobilisasi cepat regu pemadam kebakaran hutan dan lahan (karhutla).
3. **`Canal / Road Clearing`**: Pemblokiran kanal (*canal blocking*) dan penutupan akses alat berat.
4. **`Smallholder Encroachment`**: Program dialog sosial, mediasi, dan restorasi gambut berbasis masyarakat.

---

## 💡 Rekomendasi Preskriptif & Respons Lapangan

1. **Early Warning & Attribution:** Integrasikan model **CNN** langsung dengan sistem peringatan dini satelit untuk otomatis melabeli pemicu utama begitu *deforestation alert* terbit.
2. **Penegakan Hukum Tepat Sasaran:** Kirimkan personel penegak hukum secara langsung hanya pada kasus yang terprediksi sebagai *Selective Logging*, *Fire Clearing*, atau *Canal/Road Clearing*.
3. **Efisiensi Sumber Daya Patroli:** Hindari pemborosan anggaran dan personel pada area yang terprediksi sebagai pembukaan lahan swadaya masyarakat (*Smallholder Encroachment*) dengan mengalokasikannya pada pendekatan mediasi sosial.
