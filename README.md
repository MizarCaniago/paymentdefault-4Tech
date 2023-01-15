# <b>Payment Default Prediction</b>
<p> Final Project Kelompok 4 (4-Tech) - Rakamin Batch 28</p>
<p> Nama Kelompok: </p>
<ul>
    <li>Abizar Al Gifari</li>
    <li>Aliyah Nafilah</li>
    <li>Berlian Bidari</li>
    <li>Fadlan Setiadi</li>
    <li>Ferdy Santoso</li>
    <li>Ivana Joice Chandra</li>
    <li>Nuas Hadios Caniago</li>
    <li>Tanto Hari</li>
</ul>
Dataset: [Click Here](https://www.kaggle.com/reverie5/av-janata-hack-payment-default-prediction)


## <b>Summary Insight</b>
1. Banyak nasabah bank yang mengalami default di bulan berikutnya adalah 4645 orang atau sebanyak 22,12% dari total keseluruhan nasabah bank (21.000).
2. Dalam 22,12% tersebut,
<ul>
<li>Berdasarkan gender, 9,44% (1983 orang) adalah laki-laki dan 12,68% (2662 orang) adalah perempuan.</li>
<li>Berdasarkan kategori umur, 7,495% (1574 orang) berumur 20-an tahun, 7,481% (1571 orang) berumur 30-an tahun, 4,986% (1047 orang) berumur 40-an tahun, 1,871% (393 orang) berumur 50-an tahun, dan 0,286% (60 orang) berumur di atas 60 tahun.</li>
<li>Berdasarkan kategori pendidikan, 6,82% (1433 orang) lulusan graduate school, 11,167% (2345 orang) lulusan universitas (S1), 4,04% (849 orang) lulusan SMA, 0,086% (18 orang) lainnya.</li>
<li>Berdasarkan status pernikahan, 0,01% (2 orang) tidak diketahui statusnya, 10,56% (2218 orang) sudah menikah, 11,25% (2362 orang) belum menikah, dan 0,3% (63 orang) sudah bercerai.</li>
<li>Berdasarkan kategori limit, 16,61% (3488 orang) memiliki limit di bawah NTD 200.000, 4,729% (993 orang) memiliki limit di range NTD 200.000 - NTD 400.000, 0,748% (157 orang) memiliki limit di range NTD 400.000 - NTD 600.000, dan 0,033% (7 orang) memiliki limit di atas NTD 600.000.</li>
<li>Berdasarkan repayment status di bulan April - September 2005, mayoritas nasabah memiliki status 0.</li>
</ul>
3. Nasabah yang paling banyak default adalah perempuan single lulusan universitas berumur 20an dimana rata-rata limitnya adalah NTD 95.049.
4. Lebih spesifik, nasabah yang paling banyak default berumur 24 tahun dengan rata-rata limitnya adalah NTD 85.652.

## <b>Hasil Pengamatan Korelasi</b>
* Korelasi paling kuat terjadi antara kolom PAY_X dengan kolom PAY_X lainnya (X = 1,2,3,4,5,6) dan antara kolom BILL_AMTX dengan kolom BILL_AMTX lainnya (X = 1,2,3,4,5,6).
* Dari nilai korelasi antara BILL_AMT6 dengan BILL_AMT5, BILL_AMT5 dengan BILL_AMT4, BILL_AMT3 dengan BILL_AMT2, dan BILL_AMT2 dengan BILL_AMT1, didapat bahwa semakin besar jumlah tagihan kartu kredit nasabah pada bulan sebelumnya, semakin besar pula jumlah tagihan kartu kredit nasabah pada bulan berikutnya (misal jumlah tagihan pada bulan April besar, maka tagihan pada bulan Mei akan semakin besar). Begitu pula sebaliknya.
  * Hal ini dapat dipengaruhi oleh adanya bunga kartu kredit dan biaya keterlambatan pembayaran.
* Nilai korelasi antara PAY_6 dengan PAY_5 adalah 0.82, PAY_5 dengan PAY_4 berkorelasi sebesar 0.83, PAY_4 dengan PAY_3 berkorelasi sebesar 0.78, PAY_3 dengan PAY_2 berkorelasi sebesar 0.77, PAY_2 dengan PAY_1 berkorelasi sebesar 0.67.
  * Dari sini dapat dilihat bahwa hubungan antara repayment status seorang nasabah dari bulan satu ke bulan lainnya semakin lama cenderung semakin lemah (dari PAY_6 ke PAY_1).
  * Dari nilai-nilai korelasi ini didapat juga bahwa apabila di bulan sebelumnya nasabah menunggak pembayaran tagihan kartu kredit, maka di bulan berikutnya nasabah tersebut juga kemungkinan besar akan kembali menunggak. Begitu pula sebaliknya. Jika di bulan sebelumnya nasabah melakukan pembayaran tepat waktu / tidak menunggak, maka kemungkinan besar di bulan berikutnya nasabah juga tidak akan menunggak.
* Di antara kolom-kolom lainnya, kolom yang paling berkorelasi dengan variabel target adalah kolom PAY_1 yang kemudian diikuti dengan kolom PAY_2, PAY_3, PAY_4, PAY_5, dan PAY_6.
* Limit nasabah memiliki korelasi positif yang lemah (sampai dengan 0.3) dengan jumlah tagihan nasabah (BILL_AMT).
  * Ada kemungkinan semakin besar limit nasabah, semakin besar juga jumlah tagihannya. Begitu pula sebaliknya.
* Limit nasabah memiliki korelasi negatif yang lemah dengan repayment status (PAY_1 sampai PAY_6).
  * Ada kemungkinan semakin besar limit nasabah, semakin kecil nilai pada status repaymentnya. Begitu pula sebaliknya.


