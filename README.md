# praktikum5
### Nama = Sovy Aprianti
### NIM = 31241034
### Kelas = TI.24.A4
### Mata Kuliah = Bahasa Pemrograman

## Latihan Praktikum

![Screenshot 2024-11-12 043342](https://github.com/user-attachments/assets/f6c14a06-cc7d-4faf-89b9-4ec4d17208ab)

## Elemen.py

```python
list_a = [1, 2, 3, 4, 5]

print(list_a[2])

print(list_a[1:4])

print(list_a[-1])

list_a[3] = 10
print(list_a)

list_a[3:] = [11, 12, 13]
print(list_a)

list_b = list_a[:2]
print(list_b)

list_b.append("misalnya")
print(list_b)

list_b.extend([14, 15, 16])
print(list_b)

list_a.extend(list_b)
print(list_a)
```

## Code program tersebut: 


![sovyp5 1](https://github.com/user-attachments/assets/9f29653c-c880-4f0d-b9aa-71fb103106d1)

## Hasil Program tersebut:

![hasilp5 1](https://github.com/user-attachments/assets/6115c3a2-75fe-4dd3-8ffe-2bd03f438232)

## Menambah data.py

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas

    def hitung_nilai_akhir(self):
        return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3

mahasiswa = []

while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break

print("-" * 60)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 60)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 60)
```

## Penjelasan Code Menambah data

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas
```
`__init__`: Konstruktor ini digunakan untuk menginisialisasi objek Mahasiswa dengan atribut: `nama`, `nim`, `nilai_tugas`, `nilai_uts`, `nilai_uas`

```python
def hitung_nilai_akhir(self):
    return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3
```
Metode ini mengembalikan nilai akhir mahasiswa, yang merupakan rata-rata dari `nilai_tugas`, `nilai_uts`, dan `nilai_uas`.

```python
mahasiswa = []
```
Sebuah daftar kosong `mahasiswa` disiapkan untuk menyimpan objek `Mahasiswa` yang akan ditambahkan

```python
while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break
```
Meminta pengguna untuk memasukkan data mahasiswa berulang kali hingga pengguna memasukkan `t` untuk berhenti, Setiap input digunakan untuk membuat data Mahasiswa, yang kemudian ditambahkan ke dalam daftar mahasiswa

```python
print("-" * 60)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 60)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 60)
```
`Header` tabel dicetak terlebih dahulu, diikuti oleh baris-baris data untuk setiap mahasiswa, Untuk setiap mahasiswa, metode `hitung_nilai_akhir` dipanggil untuk menghitung nilai akhir, lalu data ditampilkan dalam format tabel

## Code program tersebut:

