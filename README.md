# LATIHAN 1
# 1. Apa yang harus didefinisikan sebeum membuat objek?
Sebelum membuat objek dari sebuah kelas ada beberapa hal yang harus didefinisikan terlebih dahulu yaitu:
- Kelas: Sebagai cetak biru untuk objek.
- Atribut: Untuk menyimpan data objek.
- Konstruktor: Untuk menginisialisasi objek.
- Metode: Untuk mengoperasikan atau memanipulasi data objek.
# 2. Buatlah gambar diagram class dan dua buah objek dari class Person bernama Antor dan Riko!
Diagram class
![image](https://github.com/user-attachments/assets/e6e90461-0e30-4451-9be8-cb959495a215)
Diagram objek

| Person | Nama | Jenis Kelamin | Umur |
| -------- | --- | --- | --- |
| Antor | Antor | L | 18 |
| Riko | Riko | L | 19 |
Objek Antor dan Riko adalah instance dari class Person, yang dimana atribut seperti nama, jenis kelamin, dan umur di isi biodata mereka
# 3. Buatlah gambar diagram objek AkunBank dengan instance method simpanUang, ambilUang dan cekSaldo
Diagram class
  ![image](https://github.com/user-attachments/assets/5743b4c9-d53e-4d00-bb5f-80a2692d91ac)
Diagram objek
  | Akun saya : AkunBank |
  | -------- |
  | saldo : 100000 |
  | simpanUang(500000) |
  | ambilUang(150000) |
  | cekSaldo() |

# LATIHAN 2
# Buatlah kode program java untuk:
# 1. Mendeklarasikan class Person, dengan atribut Nama, JenisKelamin, Umur
    public class Person {
    // Deklarasi atribut
    private String nama;
    private String jenisKelamin;
    private int umur;

    // Constructor untuk menginisialisasi atribut
    public Person(String nama, String jenisKelamin, int umur) {
        this.nama = nama;
        this.jenisKelamin = jenisKelamin;
        this.umur = umur;
    }
- nama: Atribut yang menyimpan nama seseorang.
- jenisKelamin: Atribut yang menyimpan jenis kelamin seseorang.
- umur: Atribut yang menyimpan umur seseorang.
Ketiga atribut ini menggunakan akses private, sehingga hanya bisa diakses dan dimodifikasi dari dalam kelas tersebut.
# 2. Buatlah dua buah objek dari class Person bernama Anton dan Riko

    // Constructor untuk menginisialisasi atribut
    public Person(String nama, String jenisKelamin, int umur) {
        this.nama = nama;
        this.jenisKelamin = jenisKelamin;
        this.umur = umur;
    }
Menginisialisasikan objek Person dengan memberikan nilai awal untuk nama, jenisKelamin, dan umur. Nilai-nilai tersebut disimpan dalam atribut kelas menggunakan keyword this untuk membedakannya dari parameter.
    // Getter dan Setter untuk atribut nama
    public String getNama() {
        return nama;
    }

    public void setNama(String nama) {
        this.nama = nama;
    }

    // Getter dan Setter untuk atribut jenisKelamin
    public String getJenisKelamin() {
        return jenisKelamin;
    }

    public void setJenisKelamin(String jenisKelamin) {
        this.jenisKelamin = jenisKelamin;
    }

    // Getter dan Setter untuk atribut umur
    public int getUmur() {
        return umur;
    }

    public void setUmur(int umur) {
        this.umur = umur;
    }

    // Method untuk menampilkan informasi tentang person
    public void tampilkanInfo() {
        System.out.println("Nama: " + nama);
        System.out.println("Jenis Kelamin: " + jenisKelamin);
        System.out.println("Umur: " + umur);
    }

    // Main method untuk menjalankan program
    public static void main(String[] args) {
        // Membuat objek Person bernama Antor dan Riko
        Person antor = new Person("Antor", "Laki-laki", 18);
        var riko = new Person("Riko", "Laki-laki", 19);

        // Menampilkan informasi untuk Antor
        System.out.println("Informasi Antor:");
        antor.tampilkanInfo();

        // Menampilkan informasi untuk Riko
        System.out.println("\nInformasi Riko:");
        riko.tampilkanInfo();
    }
    }
Lalu tampilkan methodnya, diantaranya yaitu: 
- Getter adalah method untuk mengambil nilai dari atribut.
- Setter adalah method untuk mengubah atau menetapkan nilai dari atribut.
- Method tampilkanInfo() adalah method untuk menampilkan informasi tentang seseorang (yaitu nama, jenisKelamin, dan umur) ke dalam console.
Setelah itu tampilkan main method untuk menampilkan atau menjalankan program
# hasil otput
![image](https://github.com/user-attachments/assets/8cacf0e7-e333-435e-be9a-00ea3670f71c)

# LATIHAN 3
# 1. Mendeklarasikan class AkunBank dengan instance method simpanUang, ambilUang dan cekSaldo
    // Mendeklarasikan class AkunBank
    public class AkunBank {
    // Atribut untuk menyimpan saldo
    private int saldo;
- Kelas AkunBank merepresentasikan sebuah akun bank.
- Atribut saldo adalah variabel yang menyimpan jumlah uang di dalam akun bank. Aksesnya dibatasi dengan modifier private, yang berarti hanya bisa diakses dari dalam kelas ini
# 2. Buat objek AkunBank dan tetapkan nilai saldo awal Rp. 100000, kemudian panggil 3 method tersebut dan tampilkan proses berikut: ![image](https://github.com/user-attachments/assets/c2c8dd8b-46dc-47d3-b044-39ff8af70991)
    // Constructor untuk menginisialisasi saldo awal
    public AkunBank(int saldoAwal) {
        this.saldo = saldoAwal;
    }
Menganalisiskan objek AkunBank dengan saldo awal yang diberikan sebagai parameter. Misalnya, ketika kita membuat objek dengan saldo awal Rp. 100.000, nilai tersebut akan disimpan di atribut saldo.
    // Method untuk menyimpan uang
    public void simpanUang(int jumlah) {
        saldo += jumlah;
        System.out.println("Simpan uang: Rp. " + jumlah);
        cekSaldo();
    }

    // Method untuk mengambil uang
    public void ambilUang(int jumlah) {
        if (saldo >= jumlah) {
            saldo -= jumlah;
            System.out.println("Ambil uang: Rp. " + jumlah);
        } else {
            System.out.println("Saldo tidak cukup untuk menarik Rp. " + jumlah);
        }
        cekSaldo();
    }

    // Method untuk mengecek saldo
    public void cekSaldo() {
        System.out.println("Saldo saat ini: Rp. " + saldo);
    }

    // Main method untuk menjalankan program
    public static void main(String[] args) {
        // Membuat objek AkunBank dengan saldo awal Rp. 100000
        AkunBank akun = new AkunBank(100000);

        // Menampilkan pesan selamat datang dan saldo awal
        System.out.println("Selamat Datang di Bank ABC");
        akun.cekSaldo();

        // Menyimpan uang sebesar Rp. 500000
        akun.simpanUang(500000);

        // Mengambil uang sebesar Rp. 150000
        akun.ambilUang(150000);
    }
    }
Lalu tampilkan methodnya, diantaranya yaitu:
- Method simpanUang(int jumlah) Method ini digunakan untuk menambah saldo di akun bank.
- Method ambilUang(int jumlah) Method ini digunakan untuk mengambil uang dari akun bank.
- Method cekSaldo() Method ini digunakan untuk menampilkan saldo terkini dari akun bank ke layar.
Setelah itu tampilkan main method untuk menampilkan atau menjalankan program
# hasil otput
![image](https://github.com/user-attachments/assets/09d3a930-79c9-42b6-b80b-885ada027ef0)
