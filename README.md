# praktikum4

# PROGRAM INPUT NILAI MAHASISWA


print("=========================================================================")
print("|                     PROGRAM INPUT NILAI MAHASISWA                     |")
print("=========================================================================")

nilai= []
perulangan = True

while perulangan:
    nama = input("Masukkan Nama : ")
    nim = input("Masukkan NIM : ")
    Tugas = int(input("Masukkan Nilai Tugas : "))
    Uts = int(input("Masukkan Nilai UTS : "))
    Uas = int(input("Masukkan Nilai UAS : "))

    N1=Tugas*30/100
    N2=Uts*35/100
    N3=Uas*35/100

    nilai_Akhir=Tugas+Uas+Uts
    nilai.append([nama, nim, Tugas, Uts, Uas, int(nilai_Akhir)])
    if (input("Tambah data (y/t)? ") == 't'):
        break

print("\n                           DAFTAR NILAI MAHASISWA                     ")
print("========================================================================")
print("| No |       NAMA       |    NIM   |  TUGAS  |  UTS   |  UAS  |  AKHIR |")
print("========================================================================")
i = 0
for item in nilai:
    i += 1
    print("| {no:2d} | {nama:12s} | {nim:9s} | {nilaiTugas:5d} | {nilaiUTS:5d} | {nilaiUAS:5d} | {nilaiAKHIR:6.2f} |"
          .format(no=i, nama=item[0], nim=item[1], nilaiTugas=item[2], nilaiUTS=item[3], nilaiUAS=item[4], nilaiAKHIR=item[5]))
print("======================================================================")

