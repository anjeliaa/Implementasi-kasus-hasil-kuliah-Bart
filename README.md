lindung. |
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
