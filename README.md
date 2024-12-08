# labpy8.

# TUGAS PRAKTIKUM

Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:
    
1. Method tambah() untuk menambah data
2. Method tampilkan() untuk menampilkan data
3. Method hapus(nama) untuk menghapus data berdasarkan nama
4. Method ubah(nama) untuk mengubah data berdasarkan nama
5. Buat diagram class, flowchart dan penjelasan programnya pada README.md.
6. Commit dan push repository ke github.


        class DaftarNilaiMahasiswa:
        def __init__(self):  
        self.mahasiswa = {}

        def tambah(self, nama, nilai):
        """Menambah data mahasiswa."""
        self.mahasiswa[nama] = nilai
        print(f"Data {nama} dengan nilai {nilai} berhasil ditambahkan.")

        def tampilkan(self):
        """Menampilkan semua data mahasiswa."""
        if not self.mahasiswa:
            print("Tidak ada data mahasiswa.")
        else:
            print("Daftar Nilai Mahasiswa:")
            for nama, nilai in self.mahasiswa.items():
                print(f"Nama: {nama}, Nilai: {nilai}")

        def hapus(self, nama):
        """Menghapus data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
            del self.mahasiswa[nama]
            print(f"Data {nama} berhasil dihapus.")
        else:
            print(f"Data {nama} tidak ditemukan.")

        def ubah(self, nama, nilai_baru): 
        """Mengubah data mahasiswa berdasarkan nama."""
        if nama in self.mahasiswa:
            self.mahasiswa[nama] = nilai_baru
            print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
        else:
            print(f"Data {nama} tidak ditemukan.")

        def main():
        daftar = DaftarNilaiMahasiswa()

        while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")

        pilihan = input("Pilih menu: ")

        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            try:
                nilai = int(input("Masukkan nilai mahasiswa: "))
                daftar.tambah(nama, nilai)
            except ValueError:
                print("Nilai harus berupa angka.")
        elif pilihan == '2':
            daftar.tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            daftar.hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            try:
                nilai_baru = int(input("Masukkan nilai baru: "))
                daftar.ubah(nama, nilai_baru)
            except ValueError:
                print("Nilai harus berupa angka.")
        elif pilihan == '5':
            print("Keluar dari program.")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

        if __name__ == "__main__":
        main()

   Input
   
   <img width="663" alt="pmgrmn 1" src="https://github.com/user-attachments/assets/9f92ddee-353d-4f7f-9400-ea628a25261c">
   <img width="655" alt="pmrgman 1 1" src="https://github.com/user-attachments/assets/aa0953e2-fe66-4039-8087-e9e420cfcc1d">

  Output

  <img width="256" alt="output pmrgmn 1" src="https://github.com/user-attachments/assets/73973539-6e77-41aa-b461-1e419d2977e5">
  <img width="263" alt="output pmrgman 1 1" src="https://github.com/user-attachments/assets/6373fc16-382d-4cca-b5a0-588f969e6736">

  Penjelasan

  1. Tambah Data: Menyimpan nama dan nilai mahasiswa ke dalam dictionary.
  2. Tampilkan Data: Menampilkan semua data mahasiswa dalam format daftar.
  3. Hapus Data: Menghapus data mahasiswa berdasarkan nama berdasarkan nama.
  4. Ubah Data: Mengupdate nilai mahasiswa berdasarkan nama. Program menyediakan menu interaktif berbasis teks untuk pengguna, berjalan dalam loop hingga memilih opsi       
     Keluar.

  Flowchart
 
![Gambar WhatsApp 2024-12-05 pukul 12 36 01_300f3aa2](https://github.com/user-attachments/assets/d70b5b8c-e8c2-403d-8038-75c667b9e41d)

  DIAGRAM CLASS
 
![Gambar WhatsApp 2024-12-08 pukul 14 31 25_53417d53](https://github.com/user-attachments/assets/680953ec-4ea2-44d6-9e7f-5520a676c6b1)

  Penjelasan! Atribut: mahasiswa: Dictionary untuk menyimpan data mahasiswa (nama sebagai key, nilai sebagai value). Metode:

  1. init(): Menginisialisasi atribut mahasiswa sebagai dictionary kosong.
  2. tambah(nama, nilai): Menambahkan data mahasiswa.
  3. tampilkan(): Menampilkan semua data mahasiswa.
  4. hapus(nama): Menghapus data berdasarkan nama.
  5. ubah(nama, nilai_baru): Memperbarui nilai mahasiswa.


 


