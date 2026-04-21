# 🛍️ Specs — Online Shop

> Aplikasi online shop sederhana berbasis Vanilla JavaScript, HTML5, dan Tailwind CSS.  
> Dibangun sebagai tugas UTS mata kuliah Pemrograman Web 2.

---

## 🔗 Link Demo

**Live Demo Specs Shop di GitHub Pages(https://anwari-diky.github.io/Diki_Anwari_UTS_Web2/index.html)**

> ⚠️ Ganti URL di atas dengan link GitHub Pages Anda setelah deploy.

---

## 📋 Deskripsi Project

ShopKu adalah aplikasi e-commerce sederhana yang berjalan sepenuhnya di browser tanpa backend server. Semua data disimpan menggunakan **LocalStorage** sebagai simulasi database, dan data produk dimuat dari file **JSON statis**.

Aplikasi ini mencakup alur belanja lengkap mulai dari registrasi akun, menelusuri produk, menambahkan ke keranjang, hingga checkout dan melihat riwayat pesanan. Dilengkapi juga dengan fitur bonus seperti dark mode, wishlist, notifikasi toast, pagination, dan panel admin.

**Teknologi yang digunakan:**

| Teknologi | Keterangan |
|-----------|------------|
| HTML5 | Struktur halaman |
| JavaScript ES6+ | Logic aplikasi (Vanilla, ES Modules) |
| Tailwind CSS v3 | Styling dan responsif |
| LocalStorage | Simulasi database |
| JSON | Data produk dummy |

---

## ✨ Fitur

### Fitur Wajib

| No | Fitur | Keterangan |
|----|-------|------------|
| 1 | **Autentikasi** | Login, Register, validasi email unik & password min 6 karakter, sesi tersimpan di LocalStorage |
| 2 | **Manajemen Produk** | Daftar produk dari JSON, modal detail produk, format harga Rupiah, rating bintang |
| 3 | **Pencarian & Filter** | Real-time search by nama, filter kategori, filter rentang harga min/max |
| 4 | **Keranjang Belanja** | Tambah/hapus/update quantity, total harga otomatis, badge jumlah item di navbar |
| 5 | **Checkout** | Form pengiriman (nama, alamat, no HP) dengan validasi, generate ID transaksi unik |
| 6 | **Riwayat Pesanan** | Daftar transaksi per user, modal detail pesanan lengkap |
| 7 | **UI/UX Responsif** | Mobile-first, hamburger menu, grid 1→2→3→4 kolom sesuai layar |
| 8 | **State Management** | LocalStorage untuk session, cart, orders, wishlist, theme |

### Fitur Bonus

| No | Fitur | Keterangan |
|----|-------|------------|
| 9 | **Dark Mode** | Toggle light/dark, preferensi tersimpan otomatis |
| 10 | **Wishlist** | Simpan produk favorit, tambah ke cart langsung dari wishlist |
| 11 | **Notifikasi Toast** | Feedback visual sukses (hijau), peringatan (kuning), error (merah) |
| 12 | **Pagination** | 8 produk per halaman dengan navigasi halaman |
| 13 | **Panel Admin** | CRUD produk — tambah, edit, hapus dengan konfirmasi dialog |


## 📁 Struktur Folder

```
/
├── assets/
│   └── images/products/      # Gambar produk
├── css/
│   ├── style.css             # Input Tailwind CSS
│   └── output.css            # Output CSS (generated)
├── data/
│   └── products.json         # Data produk dummy (15 produk)
├── js/
│   ├── state.js              # StateManager — abstraksi LocalStorage
│   ├── auth.js               # AuthManager — login, register, session
│   ├── product.js            # ProductManager — load & render produk
│   ├── cart.js               # CartManager — keranjang belanja
│   ├── checkout.js           # CheckoutManager — proses checkout
│   ├── orders.js             # OrderManager — riwayat pesanan
│   ├── search.js             # SearchFilter — pencarian & filter
│   ├── wishlist.js           # WishlistManager — daftar wishlist
│   ├── admin.js              # AdminManager — CRUD produk
│   ├── toast.js              # Toast — notifikasi
│   ├── theme.js              # ThemeManager — dark mode
│   ├── pagination.js         # PaginationManager — paginasi
│   ├── main.js               # Script halaman utama
│   ├── login.js              # Script halaman login
│   ├── register.js           # Script halaman register
│   ├── cart-page.js          # Script halaman cart
│   ├── checkout-page.js      # Script halaman checkout
│   ├── orders-page.js        # Script halaman orders
│   ├── wishlist-page.js      # Script halaman wishlist
│   └── admin-page.js         # Script halaman admin
├── index.html                # Halaman utama — daftar produk
├── login.html                # Halaman login
├── register.html             # Halaman register
├── cart.html                 # Halaman keranjang
├── checkout.html             # Halaman checkout
├── orders.html               # Halaman riwayat pesanan
├── wishlist.html             # Halaman wishlist
├── admin.html                # Halaman panel admin
├── package.json
├── tailwind.config.js
└── README.md
```

---

## 🗄️ LocalStorage Keys

| Key | Tipe | Keterangan |
|-----|------|------------|
| `users` | Array | Data semua akun pengguna |
| `currentUser` | Object | Data user yang sedang login |
| `cart_{userId}` | Array | Item keranjang per user |
| `orders` | Array | Semua data transaksi |
| `wishlist_{userId}` | Array | Wishlist per user |
| `theme` | String | Preferensi tema (`light`/`dark`) |
| `products_override` | Array | Override produk dari admin panel |

---

*UTS Pemrograman Web 2 — April 2026*
