# Capstone Project Modul 3: Mechine Learning Bank Campaign Marketing

# Business Problem Understanding
**Context**  

Sistem bisnis suatu bank yaitu menghimpun dana dari nasabah kemudian dikelola bank dengan meminjamkan lagi ke nasabah lain, investasi dan kegiatan operasional lainnya yang menghasilkan keuntungan.Salah satu produk keuangan bank menghimpun dana yaitu deposito berjangka. Mekanisme deposito berjangka adalah nasabah menyetor sejumlah uang di bank atau lembaga keuangan, dan uang tersebut hanya dapat ditarik setelah jangka waktu tertentu. Sebagai kompensasi, nasabah akan diberikan bunga tetap sesuai dengan jumlah nominal uang yang disetorkan. Dengan memiliki dana  yang terkunci dalam waktu tertentu bank dapat mengelola resiko likuiditas dengan lebih baik dan menjaga stabilitas keuangan mereka. 

Dengan semakin tingginya persaingan antar bank dalam menghimpun dana nasabah, selain mempertahankan nasabah lama maka bank juga membutuhkan kampanye pemasaran untuk menarik nasabah baru dengan menawarkan produk deposito berjangka. Salah satu cara pemasaran yang dilakukan adalah dengan menghubungi secara langsung melalui telepon/ seluler untuk  penawaran produk deposito. Akan tetapi, tidak semua nasabah tertarik untuk melakukan deposito sehingga terkadang biaya marketing yang dikeluarkan menjadi sia-sia.

Tim marketing ingin mengetahui nasabah mana yang berpotensi melakukan deposito sehingga dapat memaksimalkan pendapatan dari deposito dan meminimalisir biaya yang diperlukan untuk marketing.

**Problem Statement :**
Tantangan utama adalah membangun model yang membantu bank memprediksi pelanggan mana yang kemungkinan besar akan berlangganan deposito berjangka setelah kampanye pemasaran. Tujuannya adalah untuk mengurangi biaya perekrutan sambil meminimalkan risiko kehilangan calon nasabah potensial dengan fokus pada penargetan yang lebih tepat 


**Goals :** 

Maka berdasarkan permasalahan tersebut, perusahaan ingin memiliki kemampuan untuk memprediksi kemungkinan seorang nasabah akan/ingin menggunakan deposito berjangka tersebut atau tidak, sehingga dapat memfokuskan pemasaran pada nasabah yang tepat sasaran.

Dan juga, perusahaan ingin mengetahui apa/faktor/variabel apa yang membuat seorang nasabah tertarik atau tidak, sehingga mereka dapat membuat rencana yang lebih baik dalam mendekati nasabah potensial.

Saat dilakukan pengecekan hanya menggunakan rule based sederhana (Hanya dua fitur) akurasinya mencapai 38%. Maka diharapkan dengan model ML harus lebih baik dibandingkan hanya sekedar menggunakan rule based sederhana

**Analytic Approach :**

Jadi yang akan kita lakukan adalah menganalisis data untuk menemukan pola yang membedakan nasabah yang tertarik  denhgan produk deposito berjangka dan yang tidak tertarik.

Kemudian kita akan membangun model klasifikasi yang akan membantu perusahaan untuk dapat memprediksi probabilitas seorang nasabah akan/ingin menggunakan produk deposito tersebut atau tidak. potensial dengan fokus pada penargetan yang lebih tepat

**Metric Evaluation :**

Sasaran analisis adalah sebagai berikut: 

0: Tidak (Tidak tertarik dengan deposito) 

1: Ya (Tertarik membuka rekening deposito)

Type 1 error : False Positive  
Definisi : Model memprediksi ada nasabah tertarik tapi tidak melakukan deposito.
Konsekuensi: sia-sianya biaya pemasaran, waktu dan sumber daya 
Contoh perhitungan: Jika biaya untuk menghubungi satu nasabah adalah 15 dolar, maka kerugian adalah: `270×15=4050 dolar

Type 2 error : False Negative  
Definisi : Nasabah masuk kategori yang terlewatkan tapi berniat melakukan deposito.
Konsekuensi: kehilangan calon potensial.
Contoh perhitungan: Jika satu nasabah yang melakukan deposito 300 dolar , maka potensi dana nasabah yang dilewatkan adalah:`285×300=85,300 dolar.`

Berdasarkan konsekuensinya, maka sebisa mungkin yang akan kita lakukan adalah membuat model yang dapat mengurangi cost pemasaran dari perusahaan tersebut, tetapi tanpa membuat menjadi kurangnya/tidak cukup kandidat potensial yang dibutuhkan perusahaan. Jadi kita ingin sebanyak mungkin prediksi kelas positif yang benar, dengan sesedikit mungkin prediksi false positive. Jadi nanti metric utama yang akan kita gunakan adalah f1 score

