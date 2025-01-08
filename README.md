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
     data: Objek yang digunakan untuk menyimpan dan mengelola data tiket dan view: Objek yang digunakan untuk                 menampilkan dan mendapatkan input tiket dari pengguna.
4. Kelas TicketView

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
   ! [gambar1] (https://github.com/user-attachments/assets/a1e656ec-82b6-4764-a7dd-61d430a3105b)



   
   

     



     



   




