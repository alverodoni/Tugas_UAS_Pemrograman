## Tugas_UAS_Pemrograman
Program pengelolaan tiket kereta <p>
Nama: Doni Alvero <p>
Nim: 312410663 <P>
Kelas: TI.24.A.5 <P>
Jurusan: Teknik Informatika <p>
Mata Kuliah: Bahasa Pemrograman <p>

## Penjelasan Program 
1. Kelas TiketData

         def __init__(self):
              self.tickets = []
   - __init__: Ini adalah konstruktor kelas yang digunakan untuk menginisialisasi objek TicketData. Di dalamnya, atribut      tickets diinisialisasi sebagai daftar kosong.

         def add_ticket(self, ticket):
             self.tickets.append(ticket)
   - add_ticket: Metode ini digunakan untuk menambahkan objek ticket ke dalam daftar tickets. Tiket yang ditambahkan          akan disimpan dalam daftar.

         def get_tickets(self):
             return self.tickets
   - get_tickets: Metode ini mengembalikan daftar tickets yang saat ini disimpan dalam objek TicketData. Ini                  memungkinkan pengguna untuk mendapatkan semua tiket yang telah ditambahkan.
2. Import Statements:

       from data import TicketData
       from process import TicketProcess
       from view import TicketView
   - Program ini mengimpor tiga kelas: TicketData dari modul data, TicketProcess dari modul process, dan TicketView dari modul view.

   Fungsi main()
   
       def main
           data = TicketData()
           view = TicketView()
           process = TicketProcess(data, view)
   inisialisasi
   - Membuat objek TicketData untuk mengelola data tiket.
   - Membuat objek TicketView untuk menampilkan data tiket.
   - Membuat objek TicketProcess yang menggabungkan data dan view untuk menangani proses tiket.
     
   Loop Utama
   
         while True:
             print("\n1. Tambah Tiket")
             print("2. Tampilkan Tiket")
             print("3. Keluar")
    
             choice = input("Pilih opsi: ")
    
             if choice == "1":
                 process.add_ticket()
             elif choice == "2":
                 process.show_tickets()
             elif choice == "3":
                 break
             else:
                 print("Pilihan tidak valid. Silakan coba lagi.")
    - Program berjalan dalam loop while yang menampilkan menu opsi kepada pengguna.
    - Berdasarkan input pengguna (choice), metode yang sesuai dari instance TicketProcess akan dipanggil.
    - Pengguna dapat memilih opsi untuk menambah tiket, menampilkan tiket, atau keluar dari program.
    - Jika input tidak valid, sebuah pesan akan ditampilkan.
  
   Fungsi Tambahan (new_func):

       def new_func():
           data = TicketData()
           return data
   - Fungsi ini menginisialisasi dan mengembalikan instance dari TicketData. Fungsi ini mungkin digunakan di bagian lain dari kode Anda.
   
   Blok Eksekusi:

       if __name__ == "__main__":
           main()
    - Bagian ini memastikan bahwa fungsi main() akan dijalankan ketika skrip dijalankan langsung.
4. Kelas TicketProcess
   
         def __init__(self, data, view):
             self.data = data
             self.view = view
   
         def add_ticket(self):
             ticket = self.view.input_ticket()
             if ticket:
                 self.data.add_ticket(ticket)

         def show_tickets(self):
             tickets = self.data.get_tickets()
             self.view.display_tickets(tickets)

    - __init__: Konstruktor yang digunakan untuk menginisialisasi objek TicketProcess. Ini menerima dua parameter: data: Objek yang digunakan untuk menyimpan dan mengelola data tiket dan view: Objek yang digunakan untuk menampilkan dan mendapatkan input            tiket dari pengguna.
    - ticket = self.view.input_ticket(): Memanggil metode input_ticket() dari objek view untuk mendapatkan tiket baru dari input pengguna.
    - if ticket: Memeriksa apakah tiket valid (tidak kosong atau tidak None).
    - self.data.add_ticket(ticket): Jika tiket valid, tambahkan tiket ke dalam data tiket menggunakan metode add_ticket() dari objek data.
    - tickets = self.data.get_tickets(): Memanggil metode get_tickets() dari objek data untuk mendapatkan daftar semua tiket yang tersimpan.
    - self.view.display_tickets(tickets): Memanggil metode display_tickets() dari objek view untuk menampilkan daftar tiket yang diperoleh.
6. Kelas TicketView

         def input_ticket(self):
             try:
                passenger_name = input("Masukkan nama penumpang: ")
                if not passenger_name:
                    raise ValueError("Nama penumpang tidak boleh kosong")
        
                destination = input("Masukkan tujuan: ")
                if not destination:
                    raise ValueError("Tujuan tidak boleh kosong")
        
                return {"passenger_name": passenger_name, "destination": destination}
          except ValueError as e:
              print(f"Input tidak valid: {e}")
              return None
   - Fungsi: Metode ini bertujuan untuk meminta input dari pengguna mengenai nama penumpang dan tujuan perjalanan.
   - Validasi Input: Nama penumpang tidak boleh kosong. Jika kosong, akan mengangkat ValueError dan Tujuan perjalanan         tidak boleh kosong. Jika kosong, akan mengangkat ValueError.
   - Pengembalian Data: Jika input valid, metode ini mengembalikan sebuah dictionary yang berisi passenger_name dan           destination. Jika input tidak valid, mengembalikan None.
     
   Metode diaplay_tickets

          def display_tickets(self, tickets):
              print(f"{'Nama Penumpang':<20}{'Tujuan':<20}")
              print("-" * 40)
              for ticket in tickets:
              print(f"{ticket['passenger_name']:<20}{ticket['destination']:<20}")
   - Fungsi: Metode ini bertujuan untuk menampilkan data tiket yang disimpan dalam format tabel.
   - Parameter: Menerima tickets, yang merupakan daftar tiket dalam bentuk dictionary.
   - Tampilan: Menampilkan header tabel dengan kolom "Nama Penumpang" dan "Tujuan", Menampilkan garis pemisah untuk          memperjelas tampilan tabel, Melalui loop, menampilkan setiap tiket dalam daftar tickets dalam format yang rapi.
## Hasil Program 
   ! [gambar1] ![foto1](https://github.com/user-attachments/assets/bb10c29a-6b12-465f-bd69-4423016bab05)




   
   

     



     



   




