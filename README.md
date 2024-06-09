# Tujuan
Tujuan utama proyek ini adalah untuk digunakan dalam sistem manajemen kafe untuk menghitung jumlah orang di kafe secara real-time dan akurat. Lalu, menampilkan status keramaian kafe pada antarmuka pengguna.

## Teori Sederhana
SSD Detector
Kami menggunakan SSD (Single Shot Detector) dengan arsitektur MobileNet. SSD hanya memerlukan satu kali proses untuk mendeteksi objek dalam gambar. Berbeda dengan dua tahap deteksi seperti R-CNN, SSD lebih cepat.
MobileNet dirancang untuk berjalan pada perangkat dengan sumber daya terbatas seperti ponsel, kamera IP, scanner, dll. Dengan demikian, kombinasi SSD dan MobileNet menghasilkan detektor objek yang lebih cepat dan efisien.

Centroid Tracker
Centroid tracker adalah salah satu pelacak yang paling andal. Pelacak ini menghitung pusat dari kotak pembatas (bounding boxes) yang merupakan koordinat (x, y) dari objek dalam gambar. Setelah koordinat diperoleh dari SSD, pelacak menghitung pusat dari kotak tersebut dan memberikan ID unik untuk setiap objek yang terdeteksi, agar bisa dilacak di setiap frame.

# Getting Started

## Step 1: Git Clone Repository
```bash
git clone https://github.com/reksti-g14-k1/iot-ml.git
```

## Step 2: Menginstal Dependensi
```bash
pip install -r requirements.txt
```

## Step 3: Mengaktifkan Webcam
```bash
python people_counter.py --prototxt detector/MobileNetSSD_deploy.prototxt --model detector/MobileNetSSD_deploy.caffemodel
```
