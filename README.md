# Jarkom-Modul-5-ITA02-2022

Anggota Kelompok ITA02:
1. Muhammad Faris Anwari (5027201008)
2. Calvindra Laksmono Kumoro (5027201020)
3. Adinda Putri Audyna (5027201073)

Pada pengerjaan awal, kami melakukan pembagian pada setiap area untuk bisa mengetahui netmask yang akan digunakan.

![user.txt](./img/area.JPG)

<table>
    <tr>
        <td>Bagian</td>
        <td>Host</td>
        <td>Netmask</td>
        <td> Sorted Netmask</td>
    </tr>
    <tr>
        <td>A1</td>
        <td>3</td>
        <td>/29</td>
        <td>/22</td>
    </tr>
        <tr>
        <td>A2</td>
        <td>63</td>
        <td>/25</td>
        <td>/23</td>
    </tr>
        <tr>
        <td>A3</td>
        <td>701</td>
        <td>/22</td>
        <td>/24</td>
    </tr>
        <tr>
        <td>A4</td>
        <td>2</td>
        <td>/30</td>
        <td>/25</td>
    </tr>
        <tr>
        <td>A5</td>
        <td>2</td>
        <td>/30</td>
        <td>/29</td>
    </tr>
        <tr>
        <td>A6</td>
        <td>256</td>
        <td>/23</td>
        <td>/29</td>
    </tr>
        <tr>
        <td>A7</td>
        <td>201</td>
        <td>/24</td>
        <td>/30</td>
    </tr>
        <tr>
        <td>A8</td>
        <td>3</td>
        <td>/29</td>
        <td>/30</td>
    </tr>
        <tr>
        <td>Total</td>
        <td>1231</td>
        <td>/21</td>
    </tr>
</table>

Setelah dilakukan perhitungan tabel dimana membutuhkan total host sebanyak 1231 dan netmask terbesar yang dibutuhkan ialah /21, maka kita dapat menggunakan netmask /20 untuk memberikan pengalamatan IP pada subnet.

Jadi untuk NID paling atas yaitu 192.211.0.0 dengan netmask /21. Berikut ini gambar pohon sekaligus subnetting untuk pembagian IP:

![user.txt](./img/pohon.png)

Penjelasan:

- 192.211.0.0/21 dipecah menjadi 2 cabang yaitu 192.211.0.0/22 dan 192.211.4.0/22 
(jika panjangnya /21 maka addressessnya 2048, dimana 2048 itu 4 x 512 (255 merupakan max dalam 1 oktet)

- 192.211.4.0/22 dipecah menjadi 2 cabang yaitu 192.211.4.0/23 dan 192.211.6.0/23
(jika panjangnya /23 maka addressessnya 512, dimana yang mendekati 512 itu 2 x 216 = 512)


dan seterusnya hingga bagian A18. Dengan mengetahui pembagian IP, kita dapat membuat tabel pembagian Network ID dan Subnet Mask untuk mempermudah implementasi.

<table>
    <tr>
        <td>Bagian</td>
        <td>Netmask (/)</td>
        <td>Netmask</td>
        <td>Netid</td>
    </tr>
    <tr>
        <td>A1</td>
        <td>/29</td>
        <td>255.255.255.248</td>
        <td>192.211.7.128/29</td>
    </tr>
        <tr>
        <td>A2</td>
        <td>/25</td>
        <td>255.255.255.128</td>
        <td>192.211.7.0/25</td>
    </tr>
        <tr>
        <td>A3</td>
       <td>/22</td>
        <td>255.255.252.0</td>
        <td>192.211.0.0/22</td>
    </tr>
        <tr>
        <td>A4</td>
        <td>/30</td>
        <td>255.255.255.252</td>
        <td>192.211.7.144/30</td>
    </tr>
        <tr>
        <td>A5</td>
        <td>/30</td>
        <td>255.255.255.252</td>
        <td>192.211.7.148/30</td>
    </tr>
        <tr>
        <td>A6</td>
        <td>/23</td>
        <td>255.255.254.0</td>
        <td>192.211.4.0/23</td>
    </tr>
        <tr>
        <td>A7</td>
        <td>/24</td>
        <td>255.255.255.0</td>
        <td>192.211.6.0/24</td>
    </tr>
        <tr>
        <td>A8</td>
        <td>/29</td>
        <td>255.255.255.248</td>
        <td>192.211.7.136/29</td>
    </tr>
</table>