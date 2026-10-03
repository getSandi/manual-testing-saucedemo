# Test Case
---

# 1. Login

| Scenario ID  | Test Case ID | Test Case                                | Test Data                          | Langkah Pengujian                                                                  | Expected Result                                                     |
| ------------ | ------------ | ---------------------------------------- | ---------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| TS-LOGIN-001 | TC-LOGIN-001 | Login dengan username dan password valid | `standard_user` / `secret_sauce`   | 1. Masukkan username.<br>2. Masukkan password.<br>3. Klik Login.                   | Pengguna berhasil login dan diarahkan ke halaman Products.          |
| TS-LOGIN-002 | TC-LOGIN-002 | Login dengan username tidak valid        | `invalid_user` / `secret_sauce`    | 1. Masukkan username tidak valid.<br>2. Masukkan password valid.<br>3. Klik Login. | Sistem menolak login dan menampilkan pesan error.                   |
| TS-LOGIN-003 | TC-LOGIN-003 | Login dengan password tidak valid        | `standard_user` / `wrong_password` | 1. Masukkan username valid.<br>2. Masukkan password tidak valid.<br>3. Klik Login. | Sistem menolak login dan menampilkan pesan error.                   |
| TS-LOGIN-004 | TC-LOGIN-004 | Login dengan username kosong             | Username kosong / `secret_sauce`   | 1. Biarkan username kosong.<br>2. Masukkan password.<br>3. Klik Login.             | Sistem menampilkan validasi bahwa username diperlukan.              |
| TS-LOGIN-005 | TC-LOGIN-005 | Login dengan password kosong             | `standard_user` / Password kosong  | 1. Masukkan username.<br>2. Biarkan password kosong.<br>3. Klik Login.             | Sistem menampilkan validasi bahwa password diperlukan.              |
| TS-LOGIN-006 | TC-LOGIN-006 | Login menggunakan akun yang terkunci     | `locked_out_user` / `secret_sauce` | 1. Masukkan username.<br>2. Masukkan password.<br>3. Klik Login.                   | Sistem menolak login dan menampilkan pesan bahwa pengguna terkunci. |

---

# 2. Product

| Scenario ID | Test Case ID | Test Case                                                 | Test Data                        | Langkah Pengujian                                   | Expected Result                                 |
| ----------- | ------------ | --------------------------------------------------------- | -------------------------------- | --------------------------------------------------- | ----------------------------------------------- |
| TS-PROD-001 | TC-PROD-001  | Menampilkan daftar produk                                 | `standard_user` / `secret_sauce` | 1. Login ke aplikasi.<br>2. Amati halaman Products. | Daftar produk ditampilkan.                      |
| TS-PROD-002 | TC-PROD-002  | Menampilkan nama produk                                   | -                                | 1. Amati daftar produk.                             | Nama setiap produk ditampilkan.                 |
| TS-PROD-003 | TC-PROD-003  | Menampilkan harga produk                                  | -                                | 1. Amati daftar produk.                             | Harga setiap produk ditampilkan.                |
| TS-PROD-004 | TC-PROD-004  | Menampilkan gambar produk                                 | -                                | 1. Amati daftar produk.                             | Gambar produk ditampilkan.                      |
| TS-PROD-005 | TC-PROD-005  | Membuka detail produk                                     | Sauce Labs Backpack              | 1. Klik nama atau gambar produk.                    | Halaman detail produk yang dipilih ditampilkan. |
| TS-PROD-006 | TC-PROD-006  | Menambahkan produk ke shopping cart dari halaman Products | Sauce Labs Backpack              | 1. Klik Add to cart pada produk.                    | Produk ditambahkan ke shopping cart.            |

---

# 3. Product Sorting

| Scenario ID | Test Case ID | Test Case                      | Test Data           | Langkah Pengujian                                          | Expected Result                                           |
| ----------- | ------------ | ------------------------------ | ------------------- | ---------------------------------------------------------- | --------------------------------------------------------- |
| TS-SORT-001 | TC-SORT-001  | Sorting nama A-Z               | Name (A to Z)       | 1. Buka dropdown sorting.<br>2. Pilih Name (A to Z).       | Produk diurutkan berdasarkan nama dari A sampai Z.        |
| TS-SORT-002 | TC-SORT-002  | Sorting nama Z-A               | Name (Z to A)       | 1. Buka dropdown sorting.<br>2. Pilih Name (Z to A).       | Produk diurutkan berdasarkan nama dari Z sampai A.        |
| TS-SORT-003 | TC-SORT-003  | Sorting harga rendah ke tinggi | Price (low to high) | 1. Buka dropdown sorting.<br>2. Pilih Price (low to high). | Produk diurutkan berdasarkan harga terendah ke tertinggi. |
| TS-SORT-004 | TC-SORT-004  | Sorting harga tinggi ke rendah | Price (high to low) | 1. Buka dropdown sorting.<br>2. Pilih Price (high to low). | Produk diurutkan berdasarkan harga tertinggi ke terendah. |

---

# 4. Shopping Cart

| Scenario ID | Test Case ID | Test Case                                               | Test Data           | Langkah Pengujian                                                | Expected Result                                                     |
| ----------- | ------------ | ------------------------------------------------------- | ------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------- |
| TS-CART-001 | TC-CART-001  | Membuka shopping cart                                   | -                   | 1. Klik ikon shopping cart.                                      | Halaman Your Cart ditampilkan.                                      |
| TS-CART-002 | TC-CART-002  | Memastikan produk ditampilkan di shopping cart          | Sauce Labs Backpack | 1. Tambahkan produk ke cart.<br>2. Buka shopping cart.           | Produk yang dipilih ditampilkan di shopping cart.                   |
| TS-CART-003 | TC-CART-003  | Menghapus produk dari shopping cart                     | Sauce Labs Backpack | 1. Buka shopping cart.<br>2. Klik Remove.                        | Produk dihapus dari shopping cart.                                  |
| TS-CART-004 | TC-CART-004  | Memastikan jumlah item bertambah                        | Dua produk          | 1. Tambahkan produk pertama.<br>2. Tambahkan produk kedua.       | Jumlah item pada ikon shopping cart bertambah sesuai jumlah produk. |
| TS-CART-005 | TC-CART-005  | Memastikan jumlah item berkurang setelah produk dihapus | Produk dalam cart   | 1. Buka shopping cart.<br>2. Klik Remove pada salah satu produk. | Jumlah item pada shopping cart diperbarui.                          |
| TS-CART-006 | TC-CART-006  | Melanjutkan checkout dari shopping cart                 | Produk dalam cart   | 1. Buka shopping cart.<br>2. Klik Checkout.                      | Pengguna diarahkan ke halaman Checkout: Your Information.           |

---

# 5. Checkout

| Scenario ID  | Test Case ID | Test Case                                                      | Test Data                                       | Langkah Pengujian                                                                 | Expected Result                                                         |
| ------------ | ------------ | -------------------------------------------------------------- | ----------------------------------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| TS-CHECK-001 | TC-CHECK-001 | Membuka halaman checkout                                       | Produk dalam cart                               | 1. Buka cart.<br>2. Klik Checkout.                                                | Halaman Checkout: Your Information ditampilkan.                         |
| TS-CHECK-002 | TC-CHECK-002 | Checkout menggunakan informasi valid                           | First Name: Soe<br>Last Name: Kar<br>ZIP: 12345 | 1. Isi First Name.<br>2. Isi Last Name.<br>3. Isi ZIP.<br>4. Klik Continue.       | Pengguna diarahkan ke halaman Checkout: Overview.                       |
| TS-CHECK-003 | TC-CHECK-003 | Checkout dengan First Name kosong                              | First Name kosong                               | 1. Kosongkan First Name.<br>2. Isi Last Name.<br>3. Isi ZIP.<br>4. Klik Continue. | Sistem menampilkan validasi First Name diperlukan.                      |
| TS-CHECK-004 | TC-CHECK-004 | Checkout dengan Last Name kosong                               | Last Name kosong                                | 1. Isi First Name.<br>2. Kosongkan Last Name.<br>3. Isi ZIP.<br>4. Klik Continue. | Sistem menampilkan validasi Last Name diperlukan.                       |
| TS-CHECK-005 | TC-CHECK-005 | Checkout dengan ZIP kosong                                     | ZIP kosong                                      | 1. Isi First Name.<br>2. Isi Last Name.<br>3. Kosongkan ZIP.<br>4. Klik Continue. | Sistem menampilkan validasi Postal Code diperlukan.                     |
| TS-CHECK-006 | TC-CHECK-006 | Memastikan informasi produk ditampilkan pada Checkout Overview | Produk dalam cart                               | 1. Isi data checkout.<br>2. Klik Continue.                                        | Produk dan informasi order ditampilkan pada halaman Checkout: Overview. |
| TS-CHECK-007 | TC-CHECK-007 | Menyelesaikan checkout                                         | Data checkout valid                             | 1. Isi data checkout.<br>2. Klik Continue.<br>3. Klik Finish.                     | Proses checkout berhasil diselesaikan.                                  |
| TS-CHECK-008 | TC-CHECK-008 | Menampilkan konfirmasi checkout                                | Checkout berhasil                               | 1. Selesaikan checkout.<br>2. Amati halaman konfirmasi.                           | Sistem menampilkan konfirmasi bahwa pesanan berhasil.                   |

---

# 6. Logout

| Scenario ID   | Test Case ID  | Test Case                                                     | Test Data         | Langkah Pengujian                                               | Expected Result                                                    |
| ------------- | ------------- | ------------------------------------------------------------- | ----------------- | --------------------------------------------------------------- | ------------------------------------------------------------------ |
| TS-LOGOUT-001 | TC-LOGOUT-001 | Logout dari aplikasi                                          | `standard_user`   | 1. Login ke aplikasi.<br>2. Buka menu.<br>3. Klik Logout.       | Pengguna berhasil logout.                                          |
| TS-LOGOUT-002 | TC-LOGOUT-002 | Memastikan pengguna diarahkan ke halaman Login setelah logout | -                 | 1. Logout dari aplikasi.<br>2. Amati halaman.                   | Pengguna diarahkan ke halaman Login.                               |
| TS-LOGOUT-003 | TC-LOGOUT-003 | Memastikan fitur membutuhkan autentikasi setelah logout       | User sudah logout | 1. Logout.<br>2. Coba mengakses halaman yang membutuhkan login. | Pengguna tidak dapat mengakses fitur yang membutuhkan autentikasi. |

---

## Catatan

Seluruh test case akan dieksekusi secara manual menggunakan:

* Sistem Operasi: Windows 10
* Browser: Google Chrome 152
* Metode: Manual Testing
* Pendekatan: Black Box Testing

### Status test case akan diisi setelah proses eksekusi dilakukan.

Statuss yang digunakan:

* **PASS**: Actual Result sesuai dengan Expected Result.
* **FAIL**: Actual Result tidak sesuai dengan Expected Result.
* **BLOCKED**: Test case tidak dapat dijalankan karena terdapat kondisi yang menghalangi pengujian.

