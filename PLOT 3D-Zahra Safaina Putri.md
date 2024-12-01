# Menggambar Plot 3D dengan EMT
Ini adalah pengenalan plot 3D di Euler. Kita memerlukan plot 3D untuk
memvisualisasikan fungsi dua variabel.


Euler menggambar fungsi tersebut menggunakan algoritma pengurutan
untuk menyembunyikan bagian-bagian di latar belakang. Secara umum,
Euler menggunakan proyeksi pusat. Standarnya adalah dari kuadran x-y
positif ke arah titik asal x=y=z=0, tetapi sudut=0° terlihat dari arah
sumbu y. Sudut pandang dan ketinggian dapat diubah.


Euler dapat memetakan


* 
permukaan dengan bayangan dan garis level atau rentang level,

* 
awan titik-titik,

* 
kurva parametrik,

* 
permukaan implisit.


Plot 3D dari sebuah fungsi menggunakan plot3d. Cara termudah adalah
memplot ekspresi dalam x dan y. Parameter r mengatur rentang plot di
sekitar (0,0).


\>aspect(1.5); plot3d("x^2+sin(y)",-5,5,0,6\*pi):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-001.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-001.png)

1. Gambarlah plot 3d dari


$$x^3 + cos(2y)$$

dengan rentang -10,10,0,2pi dengan aspect 1


\>aspect(1); plot3d("x^3+cos(2y)",-10,10,0,2pi):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-003.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-003.png)

\>aspect(1.5); plot3d("x^2+x\*sin(y)",-5,5,0,6\*pi):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-004.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-004.png)

2. Gambarlah plot 3d dari


$$2x^2+2xsin(4y)$$

dengan rentang -10,10,0,6pi dan aspect 1


\>aspect(1); plot3d("2\*x^2+2\*x\*sin(4\*y)", -10,10,0,6\*pi):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-006.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-006.png)

Silakan lakukan modifikasi agar gambar "talang bergelombang" tersebut tidak lurus melainkan melengkung/melingkar, baik
melingkar secara mendatar maupun melingkar turun/naik (seperti papan peluncur pada kolam renang. Temukan rumusnya.


\>aspect(1.5); plot3d("x^2+sin(y)",-5,5,0,2\*pi):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-007.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-007.png)

# Fungsi dari dua Variabel

Untuk grafik sebuah fungsi, gunakan


* 
ekspresi sederhana dalam x dan y,

* 
nama fungsi dari dua variabell

* 
atau matriks data.


Standarnya adalah kisi-kisi kawat yang terisi dengan warna yang
berbeda di kedua sisi. Perhatikan bahwa jumlah default interval grid
adalah 10, namun plot menggunakan jumlah default 40x40 persegi panjang
untuk membangun permukaan. Hal ini dapat diubah.


* 
n=40, n=[40,40]: jumlah garis kisi di setiap arah

* 
grid=10, grid=[10,10]: jumlah garis grid di setiap arah.


Kami menggunakan default n=40 dan grid=10.


\>plot3d("x^2+y^2"):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-008.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-008.png)

3. Gambarlah plot 3d 


$$3x^2-3y^2$$\>plot3d("3\*x^2-3\*y^2"):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-010.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-010.png)

Interaksi pengguna dapat dilakukan dengan parameter &gt;user. Pengguna
dapat menekan tombol berikut ini.


* 
kiri, kanan, atas, bawah: memutar sudut pandang

* 
+,-: memperbesar atau memperkecil

* 
a: menghasilkan anaglyph (lihat di bawah)

* 
l: beralih memutar sumber cahaya (lihat di bawah)

* 
spasi: mengatur ulang ke default

* 
kembali: mengakhiri interaksi


\>plot3d("exp(-x^2+y^2)",\>user, ...  
\>     title="Turn with the vector keys (press return to finish)"):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-011.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-011.png)

4. Gunakan interaksi pengguna pada Soal 3


\>plot3d("exp(3\*x^2-3\*y^2)", \>user,...  
\>   title="Turn with the vector keys(press return to finish)"):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-012.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-012.png)

Rentang plot untuk fungsi dapat ditentukan dengan


* 
a, b: rentang x

* 
c, d: rentang y

* 
r: bujur sangkar simetris di sekitar (0,0).

* 
n: jumlah subinterval untuk plot.


Terdapat beberapa parameter untuk menskalakan fungsi atau mengubah
tampilan grafik.


fscale: skala untuk nilai fungsi (standarnya adalah &lt;fscale).


scale: angka atau vektor 1x2 untuk menskalakan ke arah x dan y.


frame: jenis bingkai (default 1).


\>plot3d("exp(-(x^2+y^2)/5)",r=10,n=80,fscale=4,scale=1.2,frame=3,\>user):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-013.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-013.png)

5. Gunakan rentang plot pada Soal 3


\>plot3d("exp(-(3\*x^2-3\*y^2)/4)",r=8,fscale=3,scale=1,frame=3,\>user):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-014.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-014.png)

Tampilan dapat diubah dengan berbagai cara.


* 
jarak: jarak pandang ke plot.

* 
zoom: nilai zoom.

* 
angle: sudut ke sumbu y negatif dalam radian.

* 
height: ketinggian tampilan dalam radian.


Nilai default dapat diperiksa atau diubah dengan fungsi view(). Fungsi
ini mengembalikan parameter dalam urutan di atas.


\>view


    [5,  2.6,  2,  0.4]

Jarak yang lebih dekat membutuhkan zoom yang lebih sedikit. Efeknya
lebih seperti lensa sudut lebar.


Dalam contoh berikut ini, sudut = 0 dan tinggi = 0 terlihat dari sumbu
y negatif. Label sumbu untuk y disembunyikan dalam kasus ini.


\>plot3d("x^2+y",distance=3,zoom=1,angle=pi/2,height=0):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-015.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-015.png)

6. Gambarlah plot 3d


$$3x^2+3y$$

dengan zoom 2 angle 2pi dan height 25


\>plot3d("3\*x^2+3\*y",distance=4,zoom=2,angle=2pi,height=25):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-017.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-017.png)

Plot terlihat selalu ke bagian tengah kubus plot. Anda dapat
memindahkan bagian tengah dengan parameter center.


\>plot3d("x^4+y^2",a=0,b=1,c=-1,d=1,angle=-20°,height=20°, ...  
\>     center=[0.4,0,0],zoom=5):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-018.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-018.png)

7. Ubahlah Soal 6 dengan parameter center


\>plot3d("3\*x^2+3\*y",a=0,b=1,c=-1,d=1,angle=-25,height=25,...  
\>     center=[0.4,0,0], zoom=6): // semakin besar zoom semakin membesar gambar plotnya


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-019.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-019.png)

Plot diskalakan agar sesuai dengan kubus satuan untuk dilihat. Jadi,
tidak perlu mengubah jarak atau melakukan zoom, tergantung pada ukuran
plot. Namun demikian, label mengacu ke ukuran yang sesungguhnya.


Jika Anda menonaktifkannya dengan scale=false, Anda harus berhati-hati
agar plot tetap muat di dalam jendela plotting, dengan mengubah jarak
tampilan atau zoom, dan memindahkan bagian tengahnya.


\>plot3d("5\*exp(-x^2-y^2)",r=2,<fscale,<scale,distance=13,height=50°, ...  
\>     center=[0,0,-2],frame=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-020.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-020.png)

8. Buatlah seperti contoh sebelumnya menggunakan plot 3d


$$3exp(-2*x+y^2)$$

dengan r=0.8,distance=20,height=50,center=[0,0,-2], dan frame=7


\>plot3d("3\*exp(-2\*x^2+y^2)",r=0.8,<fscale,<scale,distance=20,height=50,...  
\>     center=[0,0,-2],frame=7):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-022.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-022.png)

Plot polar juga tersedia. Parameter polar=true menggambar plot polar.
Fungsi harus tetap merupakan fungsi dari x dan y. Parameter “fscale”
menskalakan fungsi dengan skala sendiri. Jika tidak, fungsi akan
diskalakan agar sesuai dengan kubus.


\>plot3d("1/(x^2+y^2+1)",r=5,\>polar, ...  
\>   fscale=2,\>hue,n=100,zoom=4,\>contour,color=red):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-023.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-023.png)

9. Buatlah plot 3d seperti contoh di atas dengan


$$\frac {2} {x^2+y-4}$$

ketentuannya r=5,fscale=3,n=100,zoom=3, dan warnanya biru


\>plot3d("2/(x^2+y^2-4)",r=5,\>polar,...  
\>   fscale=3,\>hue,n=100,zoom=3,\>contour,color=blue):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-025.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-025.png)

\>function f(r) := exp(-r/2)\*cos(r); ...  
\>   plot3d("f(x^2+y^2)",\>polar,scale=[1,1,0.4],r=pi,frame=3,zoom=4):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-026.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-026.png)

10. Buatlah plot 3d seperti contoh di atas


$$function f(r) := exp(\frac {2} {3})sin(r)$$$$3x^2+3y^2$$

dengan ketentuan scale=[1,1,0.5],r=2pi,frame=4, dan zoom=3


\>function f(r) := exp(2r/3)\*sin(r); ...  
\>   plot3d("f(3\*x^2+3\*y^2)",\>polar,scale=[1,1,0.5],r=2\*pi,frame=4,zoom=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-029.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-029.png)

Parameter rotate memutar fungsi dalam x di sekitar sumbu x.


* 
rotate = 1: Menggunakan sumbu x

* 
rotate=2: Menggunakan sumbu z


\>plot3d("x^2+1",a=-1,b=1,rotate=true,grid=5):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-030.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-030.png)

11. Buatlah plot 3d dengan rotasi


$$7x^2+3$$

dengan a=-1,b=1,dan grid=10


\>plot3d("7\*x^2+3",a=-1,b=1,rotate=true,grid=10):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-032.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-032.png)

\>plot3d("x^2+1",a=-1,b=1,rotate=2,grid=5):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-033.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-033.png)

12. Buatlah plot rd dengan rotate=3


$$7x^2+3$$

ketentuannya a=-1,b=1, dan grid=4


\>plot3d("7\*x^2+3",a=-1,b=1,rotate=3,grid=4):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-035.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-035.png)

\>plot3d("sqrt(25-x^2)",a=0,b=5,rotate=1):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-036.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-036.png)

13. Buatlah plot3d rotate=2


$$sqrt(10-x^2)$$

dengan a=0 dan b=3


\>plot3d("sqrt(10-x^2)",a=0,b=3,rotate=2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-038.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-038.png)

\>plot3d("x\*sin(x)",a=0,b=6pi,rotate=2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-039.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-039.png)

14. Buatlah plot3d rotate=2


$$xcos(2x)$$

dengan a=0 dan b=4pi


\>plot3d("x\*cos(2x)",a=0,b=4pi,rotate=2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-041.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-041.png)

Berikut ini adalah plot dengan tiga fungsi.


\>plot3d("x","x^2+y^2","y",r=2,zoom=3.5,frame=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-042.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-042.png)

15. Buarlah plot3d dengan tiga fungsi berikut


$$x+1$$$$3x^2+4y^2$$$$y$$

dengan r=1,zoom=4, dan frame=3


\>plot3d("x+1","3\*x^2+4\*y^2","y",r=1,zoom=4,frame=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-046.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-046.png)

# Plot Kontur

Untuk plot, Euler menambahkan garis kisi-kisi. Sebagai gantinya,
dimungkinkan untuk menggunakan garis level dan rona satu warna atau
rona berwarna spektral. Euler dapat menggambar ketinggian fungsi pada
plot dengan bayangan. Pada semua plot 3D, Euler dapat menghasilkan
anaglyph merah/cyan.


* 
Rona: Mengaktifkan bayangan cahaya, bukan kabel.

* 
&gt;contour: Memplot garis kontur otomatis pada plot.

* 
level=... (atau level): Vektor nilai untuk garis kontur.


Defaultnya adalah level=“auto”, yang menghitung beberapa garis level
secara otomatis. Seperti yang Anda lihat di plot, level sebenarnya
adalah rentang level.


Gaya default dapat diubah. Untuk plot kontur berikut ini, kami
menggunakan grid yang lebih halus untuk titik 100x100, skala fungsi
dan plot, dan menggunakan sudut pandang yang berbeda.


\>plot3d("exp(-x^2-y^2)",r=2,n=100,level="thin", ...  
\>    \>contour,\>spectral,fscale=1,scale=1.1,angle=45°,height=20°):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-047.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-047.png)

16. Buatlah plo3d seperti contoh di atas


$$-3x^2-y^2$$

dengan fscale=1,scale=1.3,angle=30,height=20


\>plot3d("exp(-3\*x^2-y^2)",r=3,n=150,level="thin",...  
\>   \>contour,\>spectral,fscale=1,scale=1.3,angle=30,height=20):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-049.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-049.png)

\>plot3d("exp(x\*y)",angle=100°,\>contour,color=green):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-050.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-050.png)

17. Buatlah plot3d


$$exp(3xy)$$

dengan angle=115 dan warna biru


\>plot3d("exp(3\*x\*y)",angle=115,\>contour,color=blue):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-052.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-052.png)

Bayangan default menggunakan warna abu-abu. Tetapi, kisaran warna
spektral juga tersedia.


* 
&gt;spektral: Menggunakan skema spektral default

* 
color =...: Menggunakan warna khusus atau skema spektral


Untuk plot berikut ini, kami menggunakan skema spektral default dan
menambah jumlah titik untuk mendapatkan tampilan yang sangat mulus.


\>plot3d("x^2+y^2",\>spectral,\>contour,n=100):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-053.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-053.png)

18. Buatlah plot3d


$$3x^2+y^2$$

dengan spectral,contour, dan n=200


\>plot3d("3\*x^2+y^2",\>spectral,\>contour,n=200):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-055.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-055.png)

Alih-alih garis level otomatis, kita juga dapat menetapkan nilai garis
level. Hal ini akan menghasilkan garis level yang tipis, alih-alih
rentang level.


\>plot3d("x^2-y^2",0,5,0,5,level=-1:0.1:1,color=redgreen):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-056.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-056.png)

19. Buatlah plot3d


$$x^2-3y^2$$

dengan level -2,0.2,2


\>plot3d("x^2-3\*y^2",0,6,0,6,level=-2:0.2:2,color=greenred):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-058.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-058.png)

Pada plot berikut ini, kami menggunakan dua pita level yang sangat
luas dari -0,1 hingga 1, dan dari 0,9 hingga 1. Ini dimasukkan sebagai
matriks dengan batas-batas level sebagai kolom.


Selain itu, kami menghamparkan grid dengan 10 interval di setiap arah.


\>plot3d("x^2+y^3",level=[-0.1,0.9;0,1], ...  
\>     \>spectral,angle=30°,grid=10,contourcolor=gray):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-059.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-059.png)

20. Buatlah plot3d


$$x^3+y^2$$

dengan level -1,0.8,1


untuk contournya berwarna biru cerah


\>plot3d("x^3+y^2",level=[-1,0.8;1],...  
\>   \>spectral,angle=35,grid=8,contourcolor=lightblue):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-061.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-061.png)

Pada contoh berikut, kami memplot himpunan, di mana


$$f(x,y) = x^y-y^x = 0$$Kita menggunakan satu garis tipis untuk garis level.


\>plot3d("x^y-y^x",level=0,a=0,b=6,c=0,d=6,contourcolor=red,n=100):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-063.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-063.png)

21. Buatlah plot3d


$$f(x,y)=5x^y-2y^x$$\>plot3d("5\*x^y-2\*y^x", level=4,a=0,b=5,c=0,d=5,contourcolor=lightblue,n=95):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-065.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-065.png)

Dimungkinkan untuk menampilkan bidang kontur di bawah plot. Warna dan
jarak ke plot dapat ditentukan.


\>plot3d("x^2+y^4",\>cp,cpcolor=green,cpdelta=0.2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-066.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-066.png)

22. Buatlah plot3d


$$x^5+2y^3$$\>plot3d("x^5+2\*y^3",\>cp,cpcolor=blue,cpdelta=0.4):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-068.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-068.png)

Berikut ini beberapa gaya lainnya. Kami selalu mematikan bingkai, dan
menggunakan berbagai skema warna untuk plot dan kisi-kisi.


\>figure(2,2); ...  
\>   expr="y^3-x^2"; ...  
\>   figure(1);  ...  
\>     plot3d(expr,<frame,\>cp,cpcolor=spectral); ...  
\>   figure(2);  ...  
\>     plot3d(expr,<frame,\>spectral,grid=10,cp=2); ...  
\>   figure(3);  ...  
\>     plot3d(expr,<frame,\>contour,color=gray,nc=5,cp=3,cpcolor=greenred); ...  
\>   figure(4);  ...  
\>     plot3d(expr,<frame,\>hue,grid=10,\>transparent,\>cp,cpcolor=gray); ...  
\>   figure(0):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-069.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-069.png)

23. Buatlah figure 2,2 plot3d


$$x^3-2y^4$$\>figure(2,2); ...  
\>   expr="x^3-2\*y^4"; ...  
\>   figure(1);  ...  
\>     plot3d(expr,<frame,\>cp,cpcolor=spectral); ...  
\>   figure(2);  ...  
\>     plot3d(expr,<frame,\>spectral,grid=10,cp=2); ...  
\>   figure(3);  ...  
\>     plot3d(expr,<frame,\>contour,color=gray,nc=5,cp=3,cpcolor=greenred); ...  
\>   figure(4);  ...  
\>     plot3d(expr,<frame,\>hue,grid=10,\>transparent,\>cp,cpcolor=gray); ...  
\>   figure(0): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-071.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-071.png)

Ada beberapa skema spektral lainnya, yang diberi nomor dari 1 hingga
9. Tetapi Anda juga dapat menggunakan color=value, di mana value


* 
spectral: untuk rentang dari biru ke merah

* 
white: untuk rentang yang lebih redup

* 
yellowblue,purplegreen,blueyellow,greenred

* 
blueyellow,greenpurple,yellowblue,redgreen


\>figure(3,3); ...  
\>   for i=1:9;  ...  
\>     figure(i); plot3d("x^2+y^2",spectral=i,\>contour,\>cp,<frame,zoom=4);  ...  
\>   end; ...  
\>   figure(0):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-072.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-072.png)

24. Buatlah plot3d figure 3,3


$$3x^2-y^2$$\>figure(3,3); ...  
\>   for i=1:9;  ...  
\>     figure(i); plot3d("3\*x^2-y^2",spectral=i,\>contour,\>cp,<frame,zoom=4);  ...  
\>   end; ...  
\>   figure(0): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-074.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-074.png)

Sumber cahaya dapat diubah dengan l dan tombol kursor selama interaksi
pengguna. Ini juga dapat ditetapkan dengan parameter.


* 
light: arah cahaya

* 
amb: cahaya sekitar antara 0 dan 1


Perhatikan, bahwa program ini tidak membuat perbedaan di antara
sisi-sisi plot. Tidak ada bayangan. Untuk ini Anda akan membutuhkan
Povray.


\>plot3d("-x^2-y^2", ...  
\>     hue=true,light=[0,1,1],amb=0,user=true, ...  
\>     title="Press l and cursor keys (return to exit)"):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-075.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-075.png)

25. Buatlah plot3d seperti contoh di atas


$$x^3-y^2$$\>plot3d("x^3-y^2",...  
\>     hue=true,light=[0,2,2],amb=0,user=true, ...  
\>     title="Press l and cursor keys (return to exit)"): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-077.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-077.png)

26. Buatlah plot 3d 


$$x^3-y^2$$\>plot3d("x^3-y^2-x^2-y^2",color=rgb(0.2,0.2,0),hue=true,frame=false, ...  
\>     zoom=3,contourcolor=blue,level=-3:0.2:1,dl=0.01):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-079.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-079.png)

\>plot3d("-x^2-y^2",color=rgb(0.2,0.2,0),hue=true,frame=false, ...  
\>     zoom=3,contourcolor=red,level=-2:0.1:1,dl=0.01): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-080.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-080.png)

Warna 0 memberikan efek pelangi yang istimewa.


\>plot3d("x^2/(x^2+y^2+1)",color=0,hue=true,grid=10):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-081.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-081.png)

27. Buatlah plot3d dengan efek pelangi istimewa


$$\frac {5x^2} {2x^3+y^2+3}$$\>plot3d("5\*x^2/(2\*x^3+y^2+3)",color=0,hue=true,grid=8):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-083.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-083.png)

Permukaannya juga bisa transparan.


\>plot3d("x^2+y^2",\>transparent,grid=10,wirecolor=red):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-084.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-084.png)

28. buatlah plot3d dengan permukaan transparan


$$3x^2+y^3$$\>plot3d("3\*x^2+y^3",\>transparent,grid=8,wirecolor=blue):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-086.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-086.png)

# Plot Implisit

Ada juga plot implisit dalam tiga dimensi. Euler menghasilkan potongan
melalui objek. Fitur plot3d termasuk plot implisit. Plot-plot ini
menunjukkan himpunan nol dari sebuah fungsi dalam tiga variabel.


Solusi dari


$$f(x,y,z) = 0$$dapat divisualisasikan dalam potongan yang sejajar dengan bidang x-y,
bidang x-z, dan bidang y-z.


* 
implisit = 1: potong sejajar dengan bidang-y-z

* 
implicit = 2: memotong sejajar dengan bidang x-z

* 
implicit=4: memotong sejajar dengan bidang x-y


Tambahkan nilai-nilai ini, jika Anda mau. Pada contoh, kami memplot


$$M = \{ (x,y,z) : x^2+y^3+zy=1 \}$$\>plot3d("x^2+y^3+z\*y-1",r=5,implicit=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-089.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-089.png)

29. Buatlah plot3d


$$N = {(x,y,z):x^3-y^2+z^y+2}$$

dengan r=7 dan implicit=4


\>plot3d("x^3-y^2+z\*y+2",r=7,implicit=4):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-091.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-091.png)

\>c=1; d=1;

\>plot3d("((x^2+y^2-c^2)^2+(z^2-1)^2)\*((y^2+z^2-c^2)^2+(x^2-1)^2)\*((z^2+x^2-c^2)^2+(y^2-1)^2)-d",r=2,<frame,\>implicit,\>user):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-092.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-092.png)

30. Buatlah plot3d seperti contoh di atas


\>c=2; d=2;

\>plot3d("((x^3-y^2-c^2)^2+(z^2-1)^2)\*((y^2+z^2-c^2)^2+(x^2-1)^2)\*((z^2+x^2-c^2)^2+(y^2-1)^2)-d",r=3,<frame,\>implicit,\>user): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-093.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-093.png)

\>plot3d("x^2+y^2+4\*x\*z+z^3",\>implicit,r=2,zoom=2.5):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-094.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-094.png)

31. Buatlah plot3d


$$x^3-y^2+7xz+z^4$$

dengan r=3 dan zoom=3


\>plot3d("x^3-y^2+7\*x\*z+z^4",\>implicit,r=3,zoom=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-096.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-096.png)

# Memplot Data 3D

Sama seperti plot2d, plot3d menerima data. Untuk objek 3D, Anda perlu
menyediakan matriks nilai x, y, dan z, atau tiga fungsi atau ekspresi
fx(x,y), fy(x,y), fz(x,y).


$$\gamma(t,s) = (x(t,s),y(t,s),z(t,s))$$Karena x,y,z adalah matriks, kita mengasumsikan bahwa (t,s) berjalan
melalui kotak persegi. Hasilnya, Anda dapat memplot gambar persegi
panjang dalam ruang.


Anda dapat menggunakan bahasa matriks Euler untuk menghasilkan
koordinat secara efektif.


Pada contoh berikut, kita menggunakan vektor nilai t dan vektor kolom
nilai s untuk memparameterkan permukaan bola. Pada gambar kita dapat
menandai daerah, dalam kasus kita daerah kutub.


\>t=linspace(0,2pi,180); s=linspace(-pi/2,pi/2,90)'; ...  
\>   x=cos(s)\*cos(t); y=cos(s)\*sin(t); z=sin(s); ...  
\>   plot3d(x,y,z,\>hue, ...  
\>   color=blue,<frame,grid=[10,20], ...  
\>   values=s,contourcolor=red,level=[90°-24°;90°-22°], ...  
\>   scale=1.4,height=50°):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-098.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-098.png)

32. Buatlah plot 3d seperti contoh diatas dengan


$$x=cos(s)sin(t)$$$$y=cos(s)cos(t)$$$$z=cos(s)$$\>t=linspace(0,2pi,180); s=linspace(-pi/2,pi/2,90)'; ...  
\>   x=cos(s)\*sin(t); y=cos(s)\*cos(t); z=cos(s); ...  
\>   plot3d(x,y,z,\>hue, ...  
\>   color=red,<frame,grid=[10,20], ...  
\>   values=s,contourcolor=blue,level=[90°-24°;90°-22°], ...  
\>   scale=2,height=40): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-102.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-102.png)

Berikut ini adalah contoh, yang merupakan grafik suatu fungsi.


\>t=-1:0.1:1; s=(-1:0.1:1)'; plot3d(t,s,t\*s,grid=10):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-103.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-103.png)

33. Buatlah plot seperti di atas dengan a=-2:0.2:2 dan b=(-2:0.4:2)


\>a=-2:0.2:2; b=(-2:0.4:2)'; plot3d(a,b,a\*b,grid=7):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-104.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-104.png)

Namun demikian, kita bisa membuat segala macam permukaan. Berikut ini
adalah permukaan yang sama dengan fungsi


$$x = y \, z$$\>plot3d(t\*s,t,s,angle=180°,grid=10):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-106.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-106.png)

34. Buatlah plot 3d seperti contoh di atasa dengan angle 90 dan grid 6


\>plot3d(a\*b,a,b,angle=90,grid=6):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-107.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-107.png)

Dengan lebih banyak upaya, kita bisa menghasilkan banyak permukaan.


Dalam contoh berikut ini, kami membuat tampilan berbayang dari bola
yang terdistorsi. Koordinat yang biasa digunakan untuk bola adalah


$$\gamma(t,s) = (\cos(t)\cos(s),\sin(t)\sin(s),\cos(s))$$dengan


$$0 \le t \le 2\pi, \quad \frac{-\pi}{2} \le s \le \frac{\pi}{2}.$$Kami mengubahnya dengan sebuah faktor


$$d(t,s) = \frac{\cos(4t)+\cos(8s)}{4}.$$\>t=linspace(0,2pi,320); s=linspace(-pi/2,pi/2,160)'; ...  
\>   d=1+0.2\*(cos(4\*t)+cos(8\*s)); ...  
\>   plot3d(cos(t)\*cos(s)\*d,sin(t)\*cos(s)\*d,sin(s)\*d,hue=1, ...  
\>     light=[1,0,1],frame=0,zoom=5):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-111.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-111.png)

35. Buatlah plot 3d seperti contoh diatas


\>t=linspace(0,2pi,320); s=linspace(-pi/2,pi/2,160)'; ...  
\>   d=1+0.2\*(cos(3\*t)+sin(5\*s)); ...  
\>   plot3d(cos(t)\*cos(s)\*d,sin(t)\*cos(s)\*d,sin(s)\*d,hue=1, ...  
\>     light=[1,0,1],frame=0,zoom=4): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-112.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-112.png)

Tentu saja, awan titik juga dimungkinkan. Untuk memplot data titik
dalam ruang, kita membutuhkan tiga vektor untuk koordinat titik.


Gaya-gayanya sama seperti pada plot2d dengan points=true;


\>n=500;  ...  
\>     plot3d(normal(1,n),normal(1,n),normal(1,n),points=true,style="."):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-113.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-113.png)

36. Buatlah plot seperti contoh di atas dengan n=112 dan style
berbentuk star (*)


\>n=112;  ...  
\>     plot3d(normal(1,n),normal(1,n),normal(1,n),points=true,style="\*"): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-114.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-114.png)

Anda juga dapat memplot kurva dalam bentuk 3D. Dalam hal ini, akan
lebih mudah untuk menghitung titik-titik kurva. Untuk kurva pada
bidang, kami menggunakan urutan koordinat dan parameter wire = true.


\>t=linspace(0,8pi,500); ...  
\>   plot3d(sin(t),cos(t),t/10,\>wire,zoom=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-115.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-115.png)

37. Buatlah plot 3d seperti contoh di atas dengan
t=linspace(0,6pi,300).


untuk cos(t),sin(2t),t/24, dan zoom=4


\>t=linspace(0,6pi,300); ...  
\>   plot3d(cos(t),sin(2\*t),t/24,\>wire,zoom=4): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-116.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-116.png)

\>t=linspace(0,4pi,1000); plot3d(cos(t),sin(t),t/2pi,\>wire, ...  
\>   linewidth=3,wirecolor=blue):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-117.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-117.png)

38. Buatlah plot3d seperti contoh di atas dengan linspace(0,4pi,550).


Untuk cos(t),sin(2t),t/6pi,linewidth=4, dan berwarna merah.


\>t=linspace(0,4pi,550); plot3d(cos(t),sin(2t),t/6pi,\>wire, ...  
\>   linewidth=4,wirecolor=red): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-118.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-118.png)

\>X=cumsum(normal(3,100)); ...  
\>    plot3d(X[1],X[2],X[3],\>anaglyph,\>wire):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-119.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-119.png)

39. Buatlah plot3d seperti contoh di atas dengan normal (5,88)


\>X=cumsum(normal(5,88)); ...  
\>    plot3d(X[1],X[2],X[3],\>anaglyph,\>wire): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-120.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-120.png)

EMT juga dapat membuat plot dalam mode anaglyph. Untuk melihat plot
semacam itu, Anda memerlukan kacamata merah/cyan.


\> plot3d("x^2+y^3",\>anaglyph,\>contour,angle=30°):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-121.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-121.png)

40. Buatlah plot3d seperti contoh di atas


$$x^3-y^3+1$$\>plot3d("x^3-y^3+1",\>anaglyph,\>contour,angle=40):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-123.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-123.png)

Sering kali, skema warna spektral digunakan untuk plot. Hal ini
menekankan ketinggian fungsi.


\>plot3d("x^2\*y^3-y",\>spectral,\>contour,zoom=3.2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-124.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-124.png)

41. Buatlah plot3d seperti contoh di atas dengan


$$x^3y^4-y+x$$\>plot3d("x^3\*y^4-y+x",\>spectral,\>contour,zoom=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-126.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-126.png)

Euler juga dapat memplot permukaan yang diparameterkan, ketika
parameternya adalah nilai x, y, dan z dari gambar kisi-kisi persegi
panjang di dalam ruang.


Untuk demo berikut ini, kami menyiapkan parameter u dan v, dan
menghasilkan koordinat ruang dari parameter ini.


\>u=linspace(-1,1,10); v=linspace(0,2\*pi,50)'; ...  
\>   X=(3+u\*cos(v/2))\*cos(v); Y=(3+u\*cos(v/2))\*sin(v); Z=u\*sin(v/2); ...  
\>   plot3d(X,Y,Z,\>anaglyph,<frame,\>wire,scale=2.3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-127.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-127.png)

42. Buatlah plot 3d seperti contoh di atas dengan beberapa perubahan


\>u=linspace(-1,1,8); v=linspace(0,3\*pi,45)';...  
\>   X=(4+u\*cos(v/2))\*cos(v); Y=(4+u\*cos(v/2))\*sin(v); Z=u\*sin(v/2); ...  
\>   plot3d(X,Y,Z,\>anaglyph,<frame,\>wire,scale=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-128.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-128.png)

Berikut ini contoh yang lebih rumit, yang tampak megah dengan kacamata
merah/cyan.


\>u:=linspace(-pi,pi,160); v:=linspace(-pi,pi,400)';  ...  
\>   x:=(4\*(1+.25\*sin(3\*v))+cos(u))\*cos(2\*v); ...  
\>   y:=(4\*(1+.25\*sin(3\*v))+cos(u))\*sin(2\*v); ...  
\>    z=sin(u)+2\*cos(3\*v); ...  
\>   plot3d(x,y,z,frame=0,scale=1.5,hue=1,light=[1,0,-1],zoom=2.8,\>anaglyph):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-129.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-129.png)

43. Buatlah plot3d seperti contoh di atas dengan beberapa perubahan


\>u:=linspace(-pi,pi,100); v:=linspace(-pi,pi,350)';  ...  
\>   x:=(5\*(1+.25\*sin(2\*v))+cos(u))\*cos(3\*v); ...  
\>   y:=(5\*(1+.25\*sin(2\*v))+cos(u))\*sin(3\*v); ...  
\>    z=sin(u)+2\*cos(3\*v); ...  
\>   plot3d(x,y,z,frame=0,scale=2,hue=1,light=[2,0,-2],zoom=3,\>anaglyph): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-130.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-130.png)

# Plot Statistik

Plot batang juga dapat digunakan. Untuk ini, kita harus menyediakan


* 
x: vektor baris dengan n+1 elemen

* 
y: vektor kolom dengan n+1 elemen

* 
z: matriks nilai berukuran nxn.


z dapat lebih besar, tetapi hanya nilai nxn yang akan digunakan.


Pada contoh, pertama-tama kita menghitung nilainya. Kemudian kita
sesuaikan x dan y, sehingga vektor berada di tengah-tengah nilai yang
digunakan.


\>x=-1:0.1:1; y=x'; z=x^2+y^2; ...  
\>   xa=(x|1.1)-0.05; ya=(y\_1.1)-0.05; ...  
\>   plot3d(xa,ya,z,bar=true):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-131.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-131.png)

44. Buatlah plot 3d seperti contoh di atas


$$z=x^2+y^3$$\>x=-1:0.1:1; y=x'; z=x^2+y^3;...  
\>   xa=(x|1.1)-0.05; ya=(y\_1.1)-0.05;...  
\>   plot3d(xa,ya,z,bar=true): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-133.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-133.png)

\>x=-1:0.1:1; y=x'; z=x+y; d=zeros(size(x)); ...  
\>   plot3d(x,y,z,disconnect=2:2:20):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-134.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-134.png)

45. Buatlah plot 3d seperti contoh di atas dengan


$$z=-x+y^2$$\>x=-1:0.1:1; y=x'; z=-x+y^2; d=zeros(size(x));...  
\>   plot3d(x,y,z,disconnect=2:2:20):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-136.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-136.png)

Dimungkinkan untuk membagi plot permukaan menjadi dua bagian atau
lebih.


\> 


Jika memuat atau menghasilkan matriks data M dari file dan perlu
memplotnya dalam 3D, Anda dapat menskalakan matriks ke [-1,1] dengan
scale(M), atau menskalakan matriks dengan &gt;zscale. Hal ini dapat
dikombinasikan dengan faktor penskalaan individual yang diterapkan
sebagai tambahan.


\>i=1:20; j=i'; ...  
\>   plot3d(i\*j^2+100\*normal(20,20),\>zscale,scale=[1,1,1.5],angle=-40°,zoom=1.8):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-137.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-137.png)

46. Buatlah plot 3d seperti contoh di atas dengan normal (15,15)


\>i=1:15; j=i'; ...  
\>   plot3d(i\*j^2+70\*normal(15,15),\>zscale,scale=[1,1,1.3],angle=-30°,zoom=2): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-138.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-138.png)

\>Z=intrandom(5,100,6); v=zeros(5,6); ...  
\>   loop 1 to 5; v[#]=getmultiplicities(1:6,Z[#]); end; ...  
\>   columnsplot3d(v',scols=1:5,ccols=[1:5]):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-139.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-139.png)

47. Buatlah plot 3d seperti contoh di atas dengan intrandom (3,75,5)


\>Z=intrandom(3,75,5); v=zeros(3,5); ...  
\>   loop 1 to 3; v[#]=getmultiplicities(1:5,Z[#]); end;...  
\>   columnsplot3d(v',scols=1:3,ccols=[1:3]): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-140.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-140.png)

# Permukaan Benda Putar

\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=1.3, ...  
\>   style="#",color=red,<outline, ...  
\>   level=[-2;0],n=100):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-141.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-141.png)

48. Buatlah plot seperti contoh di atas dengan style = "/"


\>plot2d("(x^2+y^2-1)^3-x^2\*y^3",r=2, ...  
\>   style="/",color=blue,<outline, ...  
\>   level=[-3;0],n=155): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-142.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-142.png)

\>ekspresi &= (x^2+y^2-1)^3-x^2\*y^3; $ekspresi


$$\left(y^2+x^2-1\right)^3-x^2\,y^3$$\>ekspresi &= (4\*x^5+7\*y^3-x+17)^2+5\*x^2\*y^3; $ekspresi // pengekspresian dalam bahasa LaTeX


$$\left(7\,y^3+4\,x^5-x+17\right)^2+5\,x^2\,y^3$$Kami ingin memutar kurva jantung di sekitar sumbu y. Berikut ini
adalah ekspresi yang mendefinisikan jantung:


$$f(x,y)=(x^2+y^2-1)^3-x^2.y^3.$$Selanjutnya kita atur


$$x = r.cos(a),\quad y = r.sin(a).$$\>function fr(r,a) &= ekspresi with [x=r\*cos(a),y=r\*sin(a)] | trigreduce; $fr(r,a)


$$\left(r^2-1\right)^3+\frac{\left(\sin \left(5\,a\right)-\sin \left(  3\,a\right)-2\,\sin a\right)\,r^5}{16}$$\>function fr(r,a) &= ekspresi with [x=r\*cos(a),y=r\*sin(a)] | trigreduce; $fr(r,a)


$$\left(4\,\left(\frac{\cos \left(5\,a\right)\,r^5}{16}+\frac{5\,  \cos \left(3\,a\right)\,r^5}{16}+\frac{5\,\cos a\,r^5}{8}\right)+7\,  \left(\frac{3\,\sin a\,r^3}{4}-\frac{\sin \left(3\,a\right)\,r^3}{4}  \right)-\cos a\,r+17\right)^2+\frac{\left(-5\,\sin \left(5\,a\right)  +5\,\sin \left(3\,a\right)+10\,\sin a\right)\,r^5}{16}$$Hal ini memungkinkan untuk mendefinisikan fungsi numerik, yang
menyelesaikan untuk r, jika a diberikan. Dengan fungsi tersebut kita
dapat memplotkan jantung yang diputar sebagai permukaan parametrik.


\>function map f(a) := bisect("fr",0,2;a); ...  
\>   t=linspace(-pi/2,pi/2,100); r=f(t);  ...  
\>   s=linspace(pi,2pi,100)'; ...  
\>   plot3d(r\*cos(t)\*sin(s),r\*cos(t)\*cos(s),r\*sin(t), ...  
\>   \>hue,<frame,color=red,zoom=4,amb=0,max=0.7,grid=12,height=50°):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-149.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-149.png)

Berikut ini adalah plot 3D dari gambar di atas yang diputar
mengelilingi sumbu-z. Kami mendefinisikan fungsi, yang menggambarkan
objek.


\>function f(x,y,z) ...


    r=x^2+y^2;
    return (r+z^2-1)^3-r*z^3;
     endfunction
</pre>
\>plot3d("f(x,y,z)", ...  
\>   xmin=0,xmax=1.2,ymin=-1.2,ymax=1.2,zmin=-1.2,zmax=1.4, ...  
\>   implicit=1,angle=-30°,zoom=2.5,n=[10,100,60],\>anaglyph):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-150.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-150.png)

# Plot 3D Khusus

Fungsi plot3d memang bagus untuk dimiliki, tetapi tidak memenuhi semua
kebutuhan. Selain rutinitas yang lebih mendasar, Anda juga bisa
mendapatkan plot berbingkai dari objek apa pun yang Anda sukai.


Meskipun Euler bukan program 3D, namun dapat menggabungkan beberapa
objek dasar. Kami mencoba memvisualisasikan parabola dan garis
singgungnya.


\>function myplot ...


      y=-1:0.01:1; x=(-1:0.01:1)';
      plot3d(x,y,0.2*(x-0.1)/2,<scale,<frame,>hue, ..
        hues=0.5,>contour,color=orange);
      h=holding(1);
      plot3d(x,y,(x^2+y^2)/2,<scale,<frame,>contour,>hue);
      holding(h);
    endfunction
</pre>
Sekarang framedplot() menyediakan frame, dan mengatur tampilan.


\>framedplot("myplot",[-1,1,-1,1,0,1],height=0,angle=-30°, ...  
\>     center=[0,0,-0.7],zoom=3):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-151.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-151.png)

49. Buatlah plot3d seperti contoh di atasdengan


$$\frac {3x^2+y^2} {2}$$\>function myplot ...


      y=-1:0.01:1; x=(-1:0.01:1)';
      plot3d(x,y,0.2*(x-0.1)/2,<scale,<frame,>hue, ..
        hues=0.5,>contour,color=green);
      h=holding(1);
      plot3d(x,y,(3*x^2+y^2)/2,<scale,<frame,>contour,>hue);
      holding(h);
    endfunction
</pre>
\>framedplot("myplot",[-2,2,-2,2,0,2],height=0,angle=-30°, ...  
\>     center=[0,0,-0.7],zoom=2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-153.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-153.png)

\>  


Dengan cara yang sama, Anda dapat memplot bidang kontur secara manual.
Perhatikan bahwa plot3d() mengatur jendela ke fullwindow() secara
default, namun plotcontourplane() mengasumsikannya.


\>x=-1:0.02:1.1; y=x'; z=x^2-y^4;

\>function myplot (x,y,z) ...  
\>  
<pre class="udf">      zoom(2);
      wi=fullwindow();
      plotcontourplane(x,y,z,level="auto",<scale);
      plot3d(x,y,z,>hue,<scale,>add,color=white,level="thin");
      window(wi);
      reset();
    endfunction
</pre>
\>myplot(x,y,z):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-154.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-154.png)

50. Buatlah plot 3d seperti contoh di atas dengan


$$z=x^2-y^3$$\>x=-1:0.02:1.1; y=x'; z=x^2-y^3;

\>function myplot (x,y,z) ...  
\>  
<pre class="udf">      zoom(2);
      wi=fullwindow();
      plotcontourplane(x,y,z,level="auto",<scale);
      plot3d(x,y,z,>hue,<scale,>add,color=white,level="thin");
      window(wi);
      reset();
    endfunction
</pre>
\>myplot(x,y,z): 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-156.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-156.png)

# Animasi

Euler dapat menggunakan frame untuk melakukan pra-komputasi animasi.


Salah satu fungsi yang memanfaatkan teknik ini adalah rotate. Fungsi
ini dapat mengubah sudut pandang dan menggambar ulang plot 3D. Fungsi
ini memanggil addpage() untuk setiap plot baru. Akhirnya fungsi ini
menganimasikan plot tersebut.


Silakan pelajari sumber dari rotate untuk melihat lebih detail.


\>function testplot () := plot3d("x^2+y^3"); ...  
\>   rotate("testplot"); testplot():


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-157.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-157.png)

51. Buatlah plot3d seperti contoh di atas


$$3x^2+y^4$$\>function testplot () := plot3d("3\*x^2+y^4"); ...  
\>   rotate("testplot"); testplot(): 


    Press space to stop, return to end

![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-159.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-159.png)

# Menggambar Povray

Dengan bantuan file Euler povray.e, Euler dapat menghasilkan file
Povray. Hasilnya sangat bagus untuk dilihat.


Anda perlu menginstal Povray (32bit atau 64bit) dari
  <a href="http://www.povray.org/, dan meletakkan sub-direktori “bin” dari Povray ke dalam jalur lingkungan, atau mengatur variabel “defaultpovray” dengan jalur lengkap yang mengarah ke “pvengine.exe”.">http://www.povray.org/, dan meletakkan sub-direktori “bin” dari Povray ke dalam jalur lingkungan, atau mengatur variabel “defaultpovray” dengan jalur lengkap yang mengarah ke “pvengine.exe”.</a>


Antarmuka Povray dari Euler menghasilkan file Povray di direktori home
pengguna, dan memanggil Povray untuk mengurai file-file ini. Nama file
default adalah current.pov, dan direktori defaultnya adalah
eulerhome(), biasanya c:\Users\Username\Euler. Povray menghasilkan
sebuah file PNG, yang dapat dimuat oleh Euler ke dalam notebook. Untuk
membersihkan berkas-berkas ini, gunakan povclear().


Fungsi pov3d memiliki semangat yang sama dengan plot3d. Fungsi ini
dapat menghasilkan grafik dari sebuah fungsi f(x,y), atau sebuah
permukaan dengan koordinat X,Y,Z dalam bentuk matriks, termasuk
garis-garis level yang bersifat opsional. Fungsi ini memulai raytracer
secara otomatis, dan memuat adegan ke dalam notebook Euler.


Selain pov3d(), ada banyak fungsi yang menghasilkan objek Povray.
Fungsi-fungsi ini mengembalikan string, yang berisi kode Povray untuk
objek. Untuk menggunakan fungsi-fungsi ini, mulai file Povray dengan
povstart(). Kemudian gunakan writeln(...) untuk menulis objek ke file
scene. Terakhir, akhiri file dengan povend(). Secara default,
raytracer akan dimulai, dan PNG akan dimasukkan ke dalam buku catatan
Euler.


Fungsi objek memiliki parameter yang disebut “look”, yang membutuhkan
string dengan kode povray untuk tekstur dan hasil akhir objek. Fungsi
povlook() dapat digunakan untuk menghasilkan string ini. Fungsi ini
memiliki parameter untuk warna, transparansi, Phong Shading, dll.


Perhatikan bahwa Povray universe memiliki sistem koordinat lain.
Antarmuka ini menerjemahkan semua koordinat ke sistem Povray. Jadi
Anda dapat tetap berpikir dalam sistem koordinat Euler dengan z yang
mengarah vertikal ke atas, dan sumbu x, y, z di tangan kanan.


Anda perlu memuat file povray.


\>load povray;


Pastikan direktori bin povray berada di dalam path. Jika tidak, edit
variabel berikut sehingga berisi jalur ke povray yang dapat
dieksekusi.


\>defaultpovray="C:\\Program Files\\POV-Ray\\v3.7\\bin\\pvengine.exe"


    C:\Program Files\POV-Ray\v3.7\bin\pvengine.exe

Untuk kesan pertama, kita plot sebuah fungsi sederhana. Perintah
berikut ini menghasilkan file povray di direktori pengguna Anda, dan
menjalankan Povray untuk melacak sinar pada file ini.


Jika Anda memulai perintah berikut, GUI Povray akan terbuka,
menjalankan file, dan menutup secara otomatis. Karena alasan keamanan,
Anda akan ditanya, apakah Anda ingin mengizinkan file exe dijalankan.
Anda dapat menekan cancel untuk menghentikan pertanyaan lebih lanjut.
Anda mungkin harus menekan OK pada jendela Povray untuk mengetahui
dialog awal Povray.


\>plot3d("x^2+y^2",zoom=2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-160.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-160.png)

52. Buatlah plot 3d seperti contoh di atas 


$$3x^2+y^3$$\>plot3d("3\*x^2+y^3",zoom=2):


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-162.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-162.png)

53. Buatlah plot 3d di Soal 52 ke dalam pov


\>pov3d("3\*x^2+y^3",zoom=2);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-163.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-163.png)

\>pov3d("x^2+y^2",zoom=3);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-164.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-164.png)

54. Buatlah plot 3d pada Soal 52 menjadi transparan


\>pov3d("3\*x^2+y^3",axiscolor=orange,angle=30,\>anaglyph,...  
\>   look=povlook(cyan,0.1),level=-1:0.5:1,zoom=2);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-165.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-165.png)

\>pov3d("x^2+y^3",axiscolor=red,angle=-45°,\>anaglyph, ...  
\>     look=povlook(cyan,0.2),level=-1:0.5:1,zoom=3.8);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-166.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-166.png)

Kadang-kadang perlu untuk mencegah penskalaan fungsi, dan menskalakan
fungsi dengan tangan.


Kami memplot kumpulan titik pada bidang kompleks, di mana hasil kali
jarak ke 1 dan -1 sama dengan 1.


\>pov3d("((x-1)^2+y^2)\*((x+1)^2+y^2)/40",r=2, ...  
\>     angle=-120°,level=1/40,dlevel=0.005,light=[-1,1,1],height=10°,n=50, ...  
\>     <fscale,zoom=3.8);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-167.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-167.png)

# Merencanakan dengan Koordinat

Sebagai pengganti fungsi, kita dapat membuat plot dengan koordinat.
Seperti pada plot3d, kita membutuhkan tiga matriks untuk
mendefinisikan objek.


Pada contoh, kita memutar sebuah fungsi pada sumbu z.


\>function f(x) := x^3-x+1; ...  
\>   x=-1:0.01:1; t=linspace(0,2pi,50)'; ...  
\>   Z=x; X=cos(t)\*f(x); Y=sin(t)\*f(x); ...  
\>   pov3d(X,Y,Z,angle=40°,look=povlook(red,0.1),height=50°,axis=0,zoom=4,light=[10,5,15]);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-168.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-168.png)

55. Buatlah plot 3d seperti contoh di atas


$$2x^3-3x+1$$\>function f(x) := 2\*x^3-3\*x+1; ...  
\>   x=-1:0.01:1; t=linspace(0,2pi,50)'; ...  
\>   Z=x; X=cos(t)\*f(x); Y=sin(t)\*f(x); ...  
\>   pov3d(X,Y,Z,angle=30,look=povlook(blue,0.1),height=40°,axis=0,zoom=3,light=[8,5,10]); 


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-170.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-170.png)

Pada contoh berikut, kita memplot gelombang teredam. Kami menghasilkan
gelombang dengan bahasa matriks Euler.


Kami juga menunjukkan, bagaimana objek tambahan dapat ditambahkan ke
adegan pov3d. Untuk pembuatan objek, lihat contoh berikut. Perhatikan
bahwa plot3d menskalakan plot, sehingga sesuai dengan kubus satuan.


\>r=linspace(0,1,80); phi=linspace(0,2pi,80)'; ...  
\>   x=r\*cos(phi); y=r\*sin(phi); z=exp(-5\*r)\*cos(8\*pi\*r)/3;  ...  
\>   pov3d(x,y,z,zoom=6,axis=0,height=30°,add=povsphere([0.5,0,0.25],0.15,povlook(red)), ...  
\>     w=500,h=300);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-171.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-171.png)

Dengan metode bayangan canggih Povray, hanya sedikit titik yang bisa
menghasilkan permukaan yang sangat halus. Hanya pada batas-batas dan
bayangan, trik ini bisa terlihat jelas.


Untuk itu, kita perlu menambahkan vektor normal di setiap titik
matriks.


\>Z &= x^2\*y^3


    
                                     2  3
                                    x  y
    

Persamaan permukaannya adalah [x,y,Z]. Kami menghitung dua turunan
terhadap x dan y dari persamaan ini dan mengambil hasil perkalian
silang sebagai normal.


\>dx &= diff([x,y,Z],x); dy &= diff([x,y,Z],y);


Kami mendefinisikan normal sebagai hasil kali silang dari turunan ini,
dan mendefinisikan fungsi koordinat.


\>N &= crossproduct(dx,dy); NX &= N[1]; NY &= N[2]; NZ &= N[3]; N,


    
                                   3       2  2
                           [- 2 x y , - 3 x  y , 1]
    

Kami hanya menggunakan 25 poin.


\>x=-1:0.5:1; y=x';

\>pov3d(x,y,Z(x,y),angle=10°, ...  
\>     xv=NX(x,y),yv=NY(x,y),zv=NZ(x,y),<shadow);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-172.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-172.png)

Berikut ini adalah simpul Trefoil yang dibuat oleh A. Busser di
Povray. Ada versi yang lebih baik dari ini dalam contoh.


  <a href="Contoh\Simpul Trefoil.html">Simpul Trefoil</a>  

Untuk tampilan yang bagus dengan tidak terlalu banyak titik, kita
tambahkan vektor normal di sini. Kita menggunakan Maxima untuk
menghitung normal untuk kita. Pertama, tiga fungsi untuk koordinat
sebagai ekspresi simbolik.


\>X &= ((4+sin(3\*y))+cos(x))\*cos(2\*y); ...  
\>   Y &= ((4+sin(3\*y))+cos(x))\*sin(2\*y); ...  
\>   Z &= sin(x)+2\*cos(3\*y);


Kemudian dua vektor turunan terhadap x dan y.


\>dx &= diff([X,Y,Z],x); dy &= diff([X,Y,Z],y);


Sekarang yang normal, yang merupakan produk silang dari dua turunan.


\>dn &= crossproduct(dx,dy);


Kami sekarang mengevaluasi semua ini secara numerik.


\>x:=linspace(-%pi,%pi,40); y:=linspace(-%pi,%pi,100)';


Vektor normal adalah evaluasi dari ekspresi simbolik dn[i] untuk
i=1,2,3. Sintaks untuk ini adalah &amp;“ekspresi”(parameter). Ini adalah
sebuah alternatif dari metode pada contoh sebelumnya, di mana kita
mendefinisikan ekspresi simbolik NX, NY, NZ terlebih dahulu.


\>pov3d(X(x,y),Y(x,y),Z(x,y),\>anaglyph,axis=0,zoom=5,w=450,h=350, ...  
\>     <shadow,look=povlook(blue), ...  
\>     xv=&"dn[1]"(x,y), yv=&"dn[2]"(x,y), zv=&"dn[3]"(x,y));


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-173.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-173.png)

Kami juga dapat menghasilkan kisi-kisi dalam bentuk 3D.


56. Buatlah plot 3d dengan kisi kisi


\>povstart(zoom=4); ...  
\>   x=-1:0.5:1; r=1-(2\*x+1)^2/6; ...  
\>   t=(0°:30°:360°)'; y=r\*cos(t); z=r\*sin(t); ...  
\>   writeln(povgrid(x,y,z,d=0.02,dballs=0.05)); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-174.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-174.png)

\>povstart(zoom=4); ...  
\>   x=-1:0.5:1; r=1-(x+1)^2/6; ...  
\>   t=(0°:30°:360°)'; y=r\*cos(t); z=r\*sin(t); ...  
\>   writeln(povgrid(x,y,z,d=0.02,dballs=0.05)); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-175.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-175.png)

Dengan povgrid(), kurva dapat dibuat.


\>povstart(center=[0,0,1],zoom=3.6); ...  
\>   t=linspace(0,2,1000); r=exp(-t); ...  
\>   x=cos(2\*pi\*10\*t)\*r; y=sin(2\*pi\*10\*t)\*r; z=t; ...  
\>   writeln(povgrid(x,y,z,povlook(red))); ...  
\>   writeAxis(0,2,axis=3); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-176.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-176.png)

# Objek Povray

Di atas, kami menggunakan pov3d untuk memplot permukaan. Antarmuka
povray di Euler juga dapat menghasilkan objek Povray. Objek-objek ini
disimpan sebagai string di Euler, dan perlu ditulis ke file Povray.


Kita memulai output dengan povstart().


\>povstart(zoom=4);


Pertama, kita mendefinisikan tiga silinder, dan menyimpannya dalam
bentuk string di Euler.


Fungsi povx() dll. hanya mengembalikan vektor [1,0,0], yang dapat
digunakan sebagai gantinya.


\>c1=povcylinder(-povx,povx,1,povlook(red)); ...  
\>   c2=povcylinder(-povy,povy,1,povlook(yellow)); ...  
\>   c3=povcylinder(-povz,povz,1,povlook(blue)); ...  
\>  
String berisi kode Povray, yang tidak perlu kita pahami pada saat itu.


\>c2


    cylinder { &lt;0,0,-1&gt;, &lt;0,0,1&gt;, 1
     texture { pigment { color rgb &lt;0.941176,0.941176,0.392157&gt; }  } 
     finish { ambient 0.2 } 
     }

Seperti yang Anda lihat, kami menambahkan tekstur ke objek dalam tiga
warna berbeda.


Hal ini dilakukan dengan povlook(), yang mengembalikan sebuah string
dengan kode Povray yang relevan. Kita dapat menggunakan warna default
Euler, atau menentukan warna kita sendiri. Kita juga dapat menambahkan
transparansi, atau mengubah cahaya sekitar.


\>povlook(rgb(0.1,0.2,0.3),0.1,0.5)


     texture { pigment { color rgbf &lt;0.101961,0.2,0.301961,0.1&gt; }  } 
     finish { ambient 0.5 } 
    

Sekarang kita mendefinisikan objek perpotongan, dan menulis hasilnya
ke file.


\>writeln(povintersection([c1,c2,c3]));


Perpotongan tiga silinder sulit untuk divisualisasikan, jika Anda
belum pernah melihatnya.


\>povend;


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-177.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-177.png)

Fungsi-fungsi berikut ini menghasilkan fraktal secara rekursif.


Fungsi pertama menunjukkan, bagaimana Euler menangani objek Povray
sederhana. Fungsi povbox() mengembalikan sebuah string, yang berisi
koordinat kotak, tekstur dan hasil akhir.


\>function onebox(x,y,z,d) := povbox([x,y,z],[x+d,y+d,z+d],povlook());

\>function fractal (x,y,z,h,n) ...  
\>  
<pre class="udf">     if n==1 then writeln(onebox(x,y,z,h));
     else
       h=h/3;
       fractal(x,y,z,h,n-1);
       fractal(x+2*h,y,z,h,n-1);
       fractal(x,y+2*h,z,h,n-1);
       fractal(x,y,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z,h,n-1);
       fractal(x+2*h,y,z+2*h,h,n-1);
       fractal(x,y+2*h,z+2*h,h,n-1);
       fractal(x+2*h,y+2*h,z+2*h,h,n-1);
       fractal(x+h,y+h,z+h,h,n-1);
     endif;
    endfunction
</pre>
\>povstart(fade=10,<shadow);

\>fractal(-1,-1,-1,2,4);

\>povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-178.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-178.png)

Perbedaan memungkinkan pemotongan satu objek dari objek lainnya.
Seperti persimpangan, ada bagian dari objek CSG Povray.


\>povstart(light=[5,-5,5],fade=10);


Untuk demonstrasi ini, kita akan mendefinisikan sebuah objek di
Povray, alih-alih menggunakan sebuah string di Euler. Definisi akan
langsung dituliskan ke file.


Koordinat kotak -1 berarti [-1,-1,-1].


\>povdefine("mycube",povbox(-1,1));


Kita dapat menggunakan objek ini dalam povobject(), yang mengembalikan
sebuah string seperti biasa.


\>c1=povobject("mycube",povlook(red));


Kami menghasilkan kubus kedua, dan memutar serta menskalakannya
sedikit.


\>c2=povobject("mycube",povlook(yellow),translate=[1,1,1], ...  
\>     rotate=xrotate(10°)+yrotate(10°), scale=1.2);


Kemudian kita ambil selisih dari kedua objek tersebut.


\>writeln(povdifference(c1,c2));


Sekarang tambahkan tiga sumbu.


\>writeAxis(-1.2,1.2,axis=1); ...  
\>   writeAxis(-1.2,1.2,axis=2); ...  
\>   writeAxis(-1.2,1.2,axis=4); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-179.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-179.png)

# Fungsi Implisit

Povray dapat memplot himpunan di mana f(x,y,z)=0, seperti parameter
implisit di plot3d. Namun, hasilnya terlihat jauh lebih baik.


Sintaks untuk fungsi-fungsi ini sedikit berbeda. Anda tidak dapat
menggunakan output dari ekspresi Maxima atau Euler.


$$((x^2+y^2-c^2)^2+(z^2-1)^2)*((y^2+z^2-c^2)^2+(x^2-1)^2)*((z^2+x^2-c^2)^2+(y^2-1)^2)=d$$\>povstart(angle=70°,height=50°,zoom=4);

\>c=0.1; d=0.1; ...  
\>   writeln(povsurface("(pow(pow(x,2)+pow(y,2)-pow(c,2),2)+pow(pow(z,2)-1,2))\*(pow(pow(y,2)+pow(z,2)-pow(c,2),2)+pow(pow(x,2)-1,2))\*(pow(pow(z,2)+pow(x,2)-pow(0.1,2),2)+pow(pow(y,2)-1,2))-d",povlook(red)));

\>povend();


    Error : Povray error!
    
    Error generated by error() command
    
    povray:
        error("Povray error!");
    Try "trace errors" to inspect local variables after errors.
    povend:
        povray(file,w,h,aspect,exit); 

\>povstart(angle=25°,height=10°); 

\>writeln(povsurface("pow(x,2)+pow(y,2)\*pow(z,2)-1",povlook(blue),povbox(-2,2,"")));

\>povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-181.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-181.png)

\>povstart(angle=70°,height=50°,zoom=4);


Membuat permukaan implisit. Perhatikan sintaks yang berbeda dalam
ekspresi.


\>writeln(povsurface("pow(x,2)\*y-pow(y,3)-pow(z,2)",povlook(green))); ...  
\>   writeAxes(); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-182.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-182.png)

# Objek Jaring

Pada contoh ini, kami menunjukkan cara membuat objek mesh, dan
menggambarnya dengan informasi tambahan.


Kami ingin memaksimalkan xy di bawah kondisi x+y = 1 dan
mendemonstrasikan sentuhan tangensial dari garis level.


\>povstart(angle=-10°,center=[0.5,0.5,0.5],zoom=7);


Kita tidak dapat menyimpan objek dalam sebuah string seperti
sebelumnya, karena ukurannya terlalu besar. Jadi kita mendefinisikan
objek dalam file Povray menggunakan #declare. Fungsi povtriangle()
melakukan hal ini secara otomatis. Fungsi ini dapat menerima vektor
normal seperti halnya pov3d().


Berikut ini mendefinisikan objek mesh, dan menuliskannya langsung ke
dalam file.


\>x=0:0.02:1; y=x'; z=x\*y; vx=-y; vy=-x; vz=1;

\>mesh=povtriangles(x,y,z,"",vx,vy,vz);


Sekarang kita tentukan dua cakram, yang akan berpotongan dengan
permukaan.


\>cl=povdisc([0.5,0.5,0],[1,1,0],2); ...  
\>   ll=povdisc([0,0,1/4],[0,0,1],2);


Tuliskan permukaan dikurangi kedua cakram.


\>writeln(povdifference(mesh,povunion([cl,ll]),povlook(green)));


Tuliskan kedua perpotongan tersebut.


\>writeln(povintersection([mesh,cl],povlook(red))); ...  
\>   writeln(povintersection([mesh,ll],povlook(gray)));


Tulislah satu titik secara maksimal.


\>writeln(povpoint([1/2,1/2,1/4],povlook(gray),size=2\*defaultpointsize));


Tambahkan sumbu dan selesaikan.


\>writeAxes(0,1,0,1,0,1,d=0.015); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-183.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-183.png)

# Anaglyph dalam Povray

Untuk menghasilkan anaglyph untuk kacamata merah/cyan, Povray harus
dijalankan dua kali dari posisi kamera yang berbeda. Ini menghasilkan
dua file Povray dan dua file PNG, yang dimuat dengan fungsi
loadanaglyph().


Tentu saja, Anda membutuhkan kacamata merah/cyan untuk melihat contoh
berikut dengan benar.


Fungsi pov3d() memiliki tombol sederhana untuk menghasilkan anaglyph.


\>pov3d("-exp(-x^2-y^2)/2",r=2,height=45°,\>anaglyph, ...  
\>     center=[0,0,0.5],zoom=3.5);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-184.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-184.png)

Jika Anda membuat scene dengan objek, Anda harus menempatkan pembuatan
scene ke dalam suatu fungsi, dan menjalankannya dua kali dengan nilai
yang berbeda untuk parameter anaglyph.


\>function myscene ...


      s=povsphere(povc,1);
      cl=povcylinder(-povz,povz,0.5);
      clx=povobject(cl,rotate=xrotate(90°));
      cly=povobject(cl,rotate=yrotate(90°));
      c=povbox([-1,-1,0],1);
      un=povunion([cl,clx,cly,c]);
      obj=povdifference(s,un,povlook(red));
      writeln(obj);
      writeAxes();
    endfunction
</pre>
Fungsi povanaglyph() melakukan semua ini. Parameter-parameternya
seperti pada povstart() dan povend() yang digabungkan.


\>povanaglyph("myscene",zoom=4.5);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-185.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-185.png)

# Mendefinisikan Objek sendiri

Antarmuka povray Euler berisi banyak objek. Namun Anda tidak dibatasi
pada objek-objek tersebut. Anda dapat membuat objek sendiri, yang
menggabungkan objek-objek lain, atau objek yang benar-benar baru.


Kami mendemonstrasikan sebuah torus. Perintah Povray untuk ini adalah
“torus”. Jadi kita mengembalikan sebuah string dengan perintah ini dan
parameternya. Perhatikan bahwa torus selalu berpusat pada titik asal.


\>function povdonat (r1,r2,look="") ...


      return "torus {"+r1+","+r2+look+"}";
    endfunction
</pre>
Inilah torus pertama kami.


\>t1=povdonat(0.8,0.2)


    torus {0.8,0.2}

Mari kita gunakan objek ini untuk membuat torus kedua, ditranslasikan
dan diputar.


\>t2=povobject(t1,rotate=xrotate(90°),translate=[0.8,0,0])


    object { torus {0.8,0.2}
     rotate 90 *x 
     translate &lt;0.8,0,0&gt;
     }

Sekarang, kita tempatkan semua benda ini ke dalam suatu pemandangan.
Untuk tampilannya, kami menggunakan Phong Shading.


\>povstart(center=[0.4,0,0],angle=0°,zoom=3.8,aspect=1.5); ...  
\>   writeln(povobject(t1,povlook(green,phong=1))); ...  
\>   writeln(povobject(t2,povlook(green,phong=1))); ...  
\>  
 &gt;povend();  

memanggil program Povray. Namun, jika terjadi kesalahan, program ini
tidak menampilkan kesalahan. Oleh karena itu, Anda harus menggunakan


 &gt;povend(&lt;keluar);  

jika ada yang tidak berhasil. Ini akan membiarkan jendela Povray tetap
terbuka.


\>povend(h=320,w=480);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-186.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-186.png)

\>povend(h=200,w=150);


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-187.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-187.png)

Berikut adalah contoh yang lebih rumit. Kami menyelesaikan


$$Ax \le b, \quad x \ge 0, \quad c.x \to \text{Max.}$$dan menunjukkan titik-titik yang layak dan optimal dalam plot 3D.


\>A=[10,8,4;5,6,8;6,3,2;9,5,6];

\>b=[10,10,10,10]';

\>c=[1,1,1];


Pertama, mari kita periksa, apakah contoh ini memiliki solusi atau
tidak.


\>x=simplex(A,b,c,\>max,\>check)'


    [0,  1,  0.5]

Ya, benar.


Selanjutnya kita mendefinisikan dua objek. Yang pertama adalah pesawat


$$a \cdot x \le b$$\>function oneplane (a,b,look="") ...


      return povplane(a,b,look)
    endfunction
</pre>
Kemudian kita tentukan perpotongan semua setengah ruang dan kubus.


\>function adm (A, b, r, look="") ...


      ol=[];
      loop 1 to rows(A); ol=ol|oneplane(A[#],b[#]); end;
      ol=ol|povbox([0,0,0],[r,r,r]);
      return povintersection(ol,look);
    endfunction
</pre>
Sekarang, kita bisa merencanakan adegan tersebut.


\>povstart(angle=120°,center=[0.5,0.5,0.5],zoom=3.5); ...  
\>   writeln(adm(A,b,2,povlook(green,0.4))); ...  
\>   writeAxes(0,1.3,0,1.6,0,1.5); ...  
\>  
Berikut ini adalah lingkaran di sekeliling optimal.


\>writeln(povintersection([povsphere(x,0.5),povplane(c,c.x')], ...  
\>     povlook(red,0.9)));


Dan kesalahan pada arah yang optimal.


\>writeln(povarrow(x,c\*0.5,povlook(red)));


Kami menambahkan teks ke layar. Teks hanyalah sebuah objek 3D. Kita
perlu menempatkan dan memutarnya sesuai dengan pandangan kita.


\>writeln(povtext("Linear Problem",[0,0.2,1.3],size=0.05,rotate=5°)); ...  
\>   povend();


![images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-190.png](images/PLOT%203D_23030630034_Zahra%20Safaina%20Putri_MAT%20E-190.png)

# Contoh Lainnya

Anda dapat menemukan beberapa contoh lain untuk Povray di Euler dalam
file-file berikut.


  <a href="Examples/Dandelin Spheres.html">Examples/Dandelin Spheres</a>  

  <a href="Examples/Donat Math.html">Examples/Donat Math</a>  

  <a href="Examples/Trefoil Knot.html">Examples/Trefoil Knot</a>  

  <a href="Examples/Optimization by Affine Scaling.html">Examples/Optimization by Affine Scaling</a>  

