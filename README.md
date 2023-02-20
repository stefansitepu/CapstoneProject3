# HR Analytics: Telco Customer Churn 
### Created By : Stefan Adrian Sitepu


## Business Problem Understanding
**Context**  
Sebuah perusahaan bernama Telco Company  yang bergerak dalam industri Telekomunikasi ingin melakukan analisa dan evaluasi terhadap Churn dari customer yang telah berlangganan. Churn pada Telco mengindikasikan suatu situasi dimana customer telah meninggalkan pelayanan dari provider tersebut. Sebuah dataset yang merepresentasikan profil customer yang telah meninggalkan Telco Company akan dianalisa agar dapat dilakukan rekomendasi untuk mengurangi churn tersebut.

Churn :

0 : Tidak meninggalkan Telco Company

1 : Meninggalkan Telco Company

**Problem Statement :**

Telco Company merupakan perusahaan yang bergerak pada bidan telekomunikasi, yang menyediakan pelayanan provider kepada customer, sehingga customer menjadi prioritas utama terutama untuk memperoleh profit. Semakin canggihnya industri teknologi, semakin banyak perusahaan yang juga memeberikan pelayanan yang sama sepert Telco namun dengan strategi bisnis yang berbeda, sehingga berdampak terhadap tingkat churn customer di Telco. 

Sehingga penting bagi Telco untuk melakukan evaluasi terhadap customer yang sudah meninggalkan Telco agar perusahaan tetap mempertahankan customer eksisting dan tentunya dapat meningkatkan customer baru untuk beralih ke Telco.


**Goals :**

Maka berdasarkan permasalahan tersebut, perusahaan ingin memiliki kemampuan untuk memprediksi kemungkinan seorang customer akan/ingin tetap menggunakan pelayanan dari Telco atau tidak, sehingga dapat berfokus pada customer eksisting yang masih berlangganan pada Telco, dengan harapan akan meningkatkan customer baru kedepannya.

Dan juga, perusahaan ingin mengetahui apa/faktor/variabel apa yang membuat seorang customer ingin berlangganan dengan Telco atau tidak, sehingga mereka dapat membuat rencana yang lebih baik untuk meningkatkan customer baru kedepannya.

**Analytic Approach :**

Jadi yang akan kita lakukan adalah menganalisis data untuk menemukan pola yang membedakan customer yang mau tetap berlangganan dengan yang tidak.

Kemudian kita akan membangun model klasifikasi yang akan membantu perusahaan untuk dapat memprediksi probabilitas seorang customer akan/ingin berlangganan pada Telco atau tidak.

**Metric Evaluation :**

![Screenshot 2023-02-18 235921](https://user-images.githubusercontent.com/118752097/220055713-f810a631-6724-4ee2-b2ed-a0ad115064a6.png)

Type 1 error : False Positive  
Konsekuensi: potensi kehilangan customer

Type 2 error : False Negative  
Konsekuensi: sia-sianya biaya telekomunikasi kepada customer

Berdasarkan konsekuensinya, maka sebisa mungkin yang akan kita lakukan adalah membuat model yang dapat mengurangi cost biaya telekomunikasi kepada customer dari perusahaan tersebut, tetapi tanpa membuat menjadi berkurangnya customer potensial yang berlangganan. Jadi kita ingin sebanyak mungkin prediksi kelas negatif yang benar, dengan sesedikit mungkin prediksi false positive agar dapat menjaga customer untuk tetap berlangganan pada Telco Company.

Namun, model juga perlu memperhatikan false negative, karena dengan perusahaan mengeluarkan biaya telekomunikasi kepada customer yang akan churn merupakan pengeluarn biaya marekting yang sia-sia.

Jadi, model yang dicari adalah model yang memberikan prediksi akurat pada kelas positif dengan nilai Precision setinggi mungkin untuk menghindari kehilangan customer berpotensi loyal diikuti dengan nilai Recall yang juga harus sama tingginya untuk menghindari terbuangnya biaya yang dialokasikan. Maka metric utama yang akan kita gunakan adalah f1-score namun tetap memperhatikan nilai precision agar lebih tinggi dari recall. Selain itu, tujuan menggunakan f1-score adalah mengindikasikan bahwa model klasifikasi kita punya precision dan recall yang baik.

