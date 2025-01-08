## Tugas_UAS_Pemrograman
Nama : Doni Alvero <p>
Nim : 312410663 <P>
Kelas : TI.24.A.5 <P>
Jurusan : Teknik Informatika <p>

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
2. Fungsi main()
   
        data = TicketData()
        view = TicketView()
        process = TicketProcess(data, view)
   - Membuat objek TicketData untuk mengelola data tiket.
   - Membuat objek TicketView untuk menampilkan data tiket.
   - Membuat objek TicketProcess yang menggabungkan data dan view untuk menangani proses tiket.

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
    - Pengguna dapat memilih opsi untuk menambah tiket, menampilkan tiket, atau keluar dari program.

           if __name__ == "__main__":
               main()
    - Bagian ini memastikan bahwa fungsi main() akan dijalankan ketika skrip dijalankan langsung.
3. Kelas TicketProcess
   
         def __init__(self, data, view):
             self.data = data
             self.view = view
   - __init__: Konstruktor yang digunakan untuk menginisialisasi objek TicketProcess. Ini menerima dua parameter:
            - data: Objek yang digunakan untuk menyimpan dan mengelola data tiket.
            - view: Objek yang digunakan untuk menampilkan dan mendapatkan input tiket dari pengguna.
   
   

     



     



   




