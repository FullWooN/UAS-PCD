# UAS-PCD
NAMA:MUHAMMAD NAUFAL ARIEF , NIM:202231026 , KELAS:PCD B

### Penjelasan Teori
**1. Pengolahan Citra (Image Processing)**
Pengolahan citra adalah teknik untuk manipulasi citra digital dengan tujuan memperbaiki atau menganalisis citra tersebut. Teknik ini melibatkan berbagai transformasi geometris dan filter untuk meningkatkan kualitas citra atau mengekstrak informasi.
2. Pustaka yang Digunakan
•	OpenCV: Pustaka komputer visi open-source yang menyediakan alat dan fungsi untuk memproses citra dan video.
•	NumPy: Pustaka untuk komputasi numerik di Python, sering digunakan untuk manipulasi array.
•	Matplotlib: Pustaka untuk membuat visualisasi data, termasuk menampilkan citra dalam konteks pengolahan citra.
________________________________________
### Langkah-langkah dan Penjelasan 

1. Mengimpor Pustaka
•  cv2: Digunakan untuk operasi pengolahan citra seperti membaca dan memanipulasi citra.
•  numpy: Digunakan untuk manipulasi array dan operasi matematika.
•  matplotlib.pyplot: Digunakan untuk menampilkan citra dalam bentuk grafis.



![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/ff4374b6-337f-446b-9fb6-5c2c84cc5aa9)



2. Memuat Citra
cv2.imread('tes.jpeg'): Memuat citra dari jalur yang diberikan dan mengembalikan citra sebagai array NumPy.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/ae222fd4-d9a4-4012-b099-17cd4d6a2919)




3. Mengecek Apakah Citra Berhasil Dimuat
if image is None: Mengecek apakah citra berhasil dimuat. Jika tidak, maka jalur file atau file itu sendiri mungkin salah.



![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/98523789-a9ee-4a4d-9854-47d0872d163f)



4. Mengonversi Citra dari BGR ke RGB
cv2.cvtColor(image, cv2.COLOR_BGR2RGB): Mengonversi citra dari format BGR (standar OpenCV) ke format RGB (standar Matplotlib).


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/8e8bd718-d93b-4a30-b9e8-ae6511c653d4)



5. Mendefinisikan Fungsi untuk Menampilkan Citra
•  plt.figure(figsize=(15, 10)): Membuat figure baru dengan ukuran 15x10 inci.
•  plt.subplot(2, 3, i+1): Membuat subplot dalam grid 2x3 dan menempatkan citra pada posisi i+1.
•  plt.imshow(images[i]): Menampilkan citra ke subplot.
•  plt.title(titles[i]): Menambahkan judul pada subplot.
•  plt.axis('off'): Menonaktifkan sumbu untuk tampilan yang lebih bersih.
•  plt.show(): Menampilkan semua citra dan judulnya.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/a8016741-96c0-4a91-b217-490e9c6ea809)



6. Citra Asli
original_image: Menyimpan citra asli dalam format RGB.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/ed44c689-7ca2-44c9-a9f8-a6ba3585abf2)



7. Rotasi Citra
•  (h, w) = image.shape[:2]: Mendapatkan tinggi (h) dan lebar (w) citra.
•  center = (w // 2, h // 2): Menentukan titik pusat citra.
•  cv2.getRotationMatrix2D(center, 45, 1.0): Membuat matriks transformasi untuk rotasi sebesar 45 derajat.
•  cv2.warpAffine(image_rgb, M, (w, h)): Menerapkan matriks rotasi untuk mendapatkan citra yang telah diputar.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/b7514576-cb55-4226-940b-897cd16f70d5)



8. Mengubah Ukuran Citra
cv2.resize(image_rgb, (w // 4, h // 4)): Mengubah ukuran citra menjadi seperempat dari ukuran aslinya.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/f143d02c-3e84-473e-a9fd-d66c1fd90e71)



9. Memotong Citra
•  start_row, start_col: Menentukan baris dan kolom awal untuk memotong citra.
•  end_row, end_col: Menentukan baris dan kolom akhir untuk memotong citra.
•  image_rgb[start_row:end_row, start_col:end_col]: Memotong citra untuk mendapatkan area tengah 50% dari ukuran asli.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/e4434a66-d8a6-4fd3-ae35-046afb31462d)



10. Membalik Citra Secara Horizontal
cv2.flip(image_rgb, 1): Membalik citra secara horizontal. Parameter 1 menunjukkan flipping horizontal.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/2824b371-d440-4d63-80c7-648627c11274)



11. Menerjemahkan Citra
•  np.float32([[1, 0, 100], [0, 1, 50]]): Matriks transformasi untuk menerjemahkan citra 100 piksel ke kanan dan 50 piksel ke bawah.
•  cv2.warpAffine(image_rgb, M, (w, h)): Menerapkan transformasi untuk mendapatkan citra yang telah diterjemahkan.


![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/802486a9-030f-4e80-9836-cb9892ee8894)




12. Menampilkan Semua Citra
•  images: Daftar yang berisi citra yang akan ditampilkan.
•  titles: Daftar judul untuk setiap citra.
•  display_images(images, titles): Memanggil fungsi display_images untuk menampilkan semua citra dengan judul yang sesuai.





![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/1e62dc72-d99c-41a7-9615-90164121aa0b)



![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/5bc628e5-3a75-4604-a8fb-a01b9f75d42b)
![Image](https://github.com/users/FullWooN/projects/2/assets/105794758/dd2c344f-a823-4426-abcf-927a3cb935d2)





Diagram Alur Proses Pengolahan Citra
•  oad Image
• cv2.imread('tes.jpeg')
• Membaca citra dari file
• Convert to RGB
• cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
• Mengonversi dari BGR ke RGB
• Display Original Image
• Menampilkan citra asli dengan judul
• Rotate Image
• cv2.getRotationMatrix2D() dan cv2.warpAffine()
• Memutar citra
• Resize Image
• cv2.resize(image_rgb, (w // 4, h // 4))
• Mengubah ukuran citra
• Crop Image
• image_rgb[start_row:end_row, start_col:end_col]
• Memotong citra
• Flip Image
• cv2.flip(image_rgb, 1)
• Membalik citra secara horizontal
• Translate Image
• np.float32([[1, 0, 100], [0, 1, 50]]) dan cv2.warpAffine()
• Menerjemahkan citra
• Display All Images
•Menampilkan citra yang telah diproses dengan judul yang sesuai
Kesimpulan
Dengan memahami teori dasar pengolahan citra dan langkah-langkah kode, Anda dapat melakukan berbagai operasi dasar pada citra seperti rotasi, perubahan ukuran, pemotongan, pembalikan, dan penerjemahan. Ini adalah fondasi untuk teknik yang lebih canggih dalam pemrosesan citra.
Jika Anda memiliki pertanyaan lebih lanjut atau membutuhkan informasi tambahan, jangan ragu untuk bertanya!

