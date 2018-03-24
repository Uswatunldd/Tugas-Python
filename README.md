# Tugas-Python
Tugas python untuk mempelajari daftar nilai mahasiswa.

Tugas ini menjelaskan tentang bagaimana python dapat membuat aplikasi cara menghitung data nilai mahasiswa suatu universitas. Dalam kesempatan kali ini, saya akan mencoba untuk menjelaskan seperti apa source code nya dalam python.
Untuk memulainya kita harus menggunakan library texttable dan pendukungnya menggunakan pip.
untung source code nya sebagai berikut :

from texttable import Texttable
table = Texttable()
jawab = "y"
no = 0
nama = []
nim = []
n_tugas = []
n_uts = []
n_uas = []

while (jawab == "y"):
    nama.append (input("Nama        : "))
    nim.append (input ("NIM         : "))
    n_tugas.append (input("Nilai Tugas : "))
    n_uts.append (input("Nilai UTS   : "))
    n_uas.append (input("Nilai UAS   : "))
    jawab = input("Tambah Data (y/t) ? ")
    no += 1

for i in range (no):
    nt = int (n_tugas[i])
    nu = int (n_uts[i])
    na = int (n_uas[i])
    akhir = (nt*30/100)+(nu*35/100)+(na*35/100)
    table.add_rows([['No','Nama','NIM','Tugas','UTS','UAS','Akhir'],
                    [i+1, nama[i],nim[i],n_tugas[i],n_uts[i],n_uas[i],akhir]])
print(table.draw())

Di sini saya menggunakan python 3.4.
setelah di run, tampilannya akan seperti ini :

Nama        : Uswah
NIM         : 31171077
Nilai Tugas : 90
Nilai UTS   : 89
Nilai UAS   : 90
Tambah Data (y/t) ? t
+----+-------+----------+-------+-----+-----+--------+
| No | Nama  |   NIM    | Tugas | UTS | UAS | Akhir  |
+====+=======+==========+=======+=====+=====+========+
| 1  | Uswah | 31171077 | 90    | 89  | 90  | 89.650 |
+----+-------+----------+-------+-----+-----+--------+

Terima kasih.



