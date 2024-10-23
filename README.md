Nama: Fahmi Arifin     
NIM : 312310662

# Praktikum 3 

## Deskripsi Program

Program ini adalah sistem manajemen pegawai sederhana yang ditulis dalam bahasa pemrograman **Java**. Program ini menunjukkan penggunaan pewarisan (inheritance) dalam OOP (Object Oriented Programming) dengan dua jenis pegawai: **Manager** dan **Programmer**. Keduanya mewarisi atribut dasar dari kelas `Pegawai`, dengan tambahan atribut masing-masing seperti `tunjangan` untuk **Manager** dan `bonus` untuk **Programmer**.

### Fitur Program

- **Pegawai**: Kelas dasar yang menyimpan informasi nama dan gaji pokok.
- **Manager**: Subkelas dari `Pegawai` yang memiliki tambahan atribut `tunjangan`.
- **Programmer**: Subkelas dari `Pegawai` yang memiliki tambahan atribut `bonus`.
- Method untuk mencetak informasi pegawai, termasuk atribut khusus seperti `tunjangan` dan `bonus`.

## Kodingan

![Cuplikan layar 2024-10-23 144022](https://github.com/user-attachments/assets/22ed5003-26cc-4804-a201-5a846ed837c0)

### Pegawai.java
```
// Kelas Pegawai
public class Pegawai {
    private String nama;
    private double gajiPokok;

    // Constructor
    public Pegawai(String nama, double gajiPokok) {
        this.nama = nama;
        this.gajiPokok = gajiPokok;
    }

    // Setter untuk nama
    public void setNama(String nama) {
        this.nama = nama;
    }

    // Getter untuk nama
    public String getNama() {
        return nama;
    }

    // Setter untuk gajiPokok
    public void setGajiPokok(double gajiPokok) {
        this.gajiPokok = gajiPokok;
    }

    // Getter untuk gajiPokok
    public double getGajiPokok() {
        return gajiPokok;
    }

    // Method untuk mencetak informasi pegawai
    public void cetakInfo() {
        System.out.println("Nama: " + nama);
        System.out.println("Gaji Pokok: " + gajiPokok);
    }
}

// Kelas Manager yang mewarisi dari Pegawai
class Manager extends Pegawai {
    private double tunjangan;

    // Constructor
    public Manager(String nama, double gajiPokok, double tunjangan) {
        super(nama, gajiPokok); // Memanggil constructor superclass
        this.tunjangan = tunjangan;
    }

    // Setter untuk tunjangan
    public void setTunjangan(double tunjangan) {
        this.tunjangan = tunjangan;
    }

    // Getter untuk tunjangan
    public double getTunjangan() {
        return tunjangan;
    }

    // Override cetakInfo untuk menambahkan tunjangan
    @Override
    public void cetakInfo() {
        super.cetakInfo(); // Memanggil cetakInfo dari superclass
        System.out.println("Tunjangan: " + tunjangan);
    }

    // Method untuk mencetak tunjangan
    public void cetakTunjangan() {
        System.out.println("Tunjangan: " + tunjangan);
    }
}

// Kelas Programmer yang mewarisi dari Pegawai
class Programmer extends Pegawai {
    private double bonus;

    // Constructor
    public Programmer(String nama, double gajiPokok, double bonus) {
        super(nama, gajiPokok); // Memanggil constructor superclass
        this.bonus = bonus;
    }

    // Setter untuk bonus
    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    // Getter untuk bonus
    public double getBonus() {
        return bonus;
    }

    // Override cetakInfo untuk menambahkan bonus
    @Override
    public void cetakInfo() {
        super.cetakInfo(); // Memanggil cetakInfo dari superclass
        System.out.println("Bonus: " + bonus);
    }

    // Method untuk mencetak bonus
    public void cetakBonus() {
        System.out.println("Bonus: " + bonus);
    }
}






