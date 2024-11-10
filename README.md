
# Aplikasi Penghitung Hari    

Latihan 1 - Muhammad Raihan Fadhillah 2210010404

## Daftar Isi
- [Deskripsi](#deskripsi)
- [Prerequisites](#prerequisites)
- [Fitur](#fitur)
- [Cara Menjalankan](#cara-menjalankan)
- [Dokumentasi](#dokumentasi)
- [Screenshots](#screenshots)
- [Contoh Penggunaan](#contoh-penggunaan)
- [Pembuat](#pembuat)

## Deskripsi
Aplikasi Pertambahan Dua Angka adalah aplikasi berbasis Java yang memungkinkan pengguna untuk menjumlahkan dua angka. Aplikasi ini memiliki antarmuka pengguna grafis (GUI) yang sederhana dan intuitif, menggunakan komponen Swing. Pengguna dapat memasukkan dua angka, dan setelah menekan tombol "Tambah", hasil penjumlahannya akan ditampilkan. Aplikasi ini juga menyediakan tombol untuk menghapus input dan keluar dari aplikasi.

## Prerequisites
- JDK versi 8 atau lebih baru.
- IDE seperti IntelliJ IDEA, Eclipse, atau NetBeans untuk menjalankan dan mengembangkan aplikasi.

## Fitur
1. Menjumlahkan dua angka yang dimasukkan oleh pengguna.
2. Menampilkan hasil penjumlahan di field hasil.
3. Memvalidasi input untuk memastikan hanya angka yang dapat dimasukkan.
4. Tombol untuk menghapus semua input dengan mudah.

## Cara Menjalankan
1. Clone atau Download Repository:
    - Clone repository ini atau download sebagai ZIP dan ekstrak.

2. Buka Proyek di IDE:
    - Buka IDE Anda dan import proyek Java yang telah diunduh.

3. Jalankan Aplikasi:
    - Jalankan kelas PertambahanDuaAngka dari IDE Anda.

## Dokumentasi
- Method konstruktor
``` java
public PertambahanDuaAngka() {
        initComponents();
    }
```

- Method hitung 
``` java
private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        try {
            int angka1 = Integer.parseInt(jTextField1.getText());
            int angka2 = Integer.parseInt(jTextField2.getText());
            int hasil = angka1 + angka2;
            jTextFieldHasil.setText(String.valueOf(hasil));
            } catch (NumberFormatException e) {
                JOptionPane.showMessageDialog(null, "Masukkan hanya angka!", "Error", JOptionPane.ERROR_MESSAGE);
            }

    }    
```

- Method reset
``` java
 private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        jTextField1.setText("");
        jTextField2.setText("");
        jTextFieldHasil.setText("");
        jTextField1.requestFocus();
    }         
```

- Method exit
``` java
 private void jButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        // TODO add your handling code here:
        System.exit(0);
    } 
```

- Method key adapter
``` java
private void jTextField1KeyTyped(java.awt.event.KeyEvent evt) {                                     
        // TODO add your handling code here:
        char input = evt.getKeyChar();
        if (!Character.isDigit(input)) {
            evt.consume();  // Mencegah input selain angka
        }
    }                                    

    private void jTextField2KeyTyped(java.awt.event.KeyEvent evt) {                                     
        // TODO add your handling code here:
        char input = evt.getKeyChar();
        if (!Character.isDigit(input)) {
            evt.consume();  // Mencegah input selain angka
        }
    }                
```

- Method focus gained
``` java
 private void jTextField1FocusGained(java.awt.event.FocusEvent evt) {                                        
        // TODO add your handling code here:
        jTextField1.setText("");
    }                                       

    private void jTextField2FocusGained(java.awt.event.FocusEvent evt) {                                        
        // TODO add your handling code here:
        jTextField2.setText("");
    }                    
```
## Screenshots
![Screenshot 2024-11-10 181016](https://github.com/user-attachments/assets/9483597b-0453-4c13-b683-37b290dc1898)


## Contoh Penggunaan
1. Masukkan angka pada dua field yang disediakan.
2. Klik tombol 'tambah' untuk menambahkan dua angka dan menampilkan hasil pada field hasil.
3. Klik tombol 'hapus' untuk mereset semua field.
4. Klik tombol 'keluar' untuk keluar dari aplikasi.


## Pembuat

- Nama : Muhammad Raihan Fadhillah
- NPM : 2210010404
