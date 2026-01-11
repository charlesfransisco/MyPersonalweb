# 🚀 Panduan Push ke GitHub

## Langkah-langkah Push Project ke GitHub

### **Langkah 1: Buat Repository di GitHub**
1. Buka [github.com](https://github.com) dan login
2. Klik tombol **"+"** di pojok kanan atas → pilih **"New repository"**
3. Isi:
   - **Repository name**: `MyWeb` (atau nama lain)
   - **Description**: (opsional) "Personal Website Portfolio"
   - **Visibility**: Pilih Public atau Private
   - **JANGAN** centang "Initialize with README" (karena sudah ada file)
4. Klik **"Create repository"**

### **Langkah 2: Inisialisasi Git di Local**
Buka terminal di folder project Anda (`D:\Github\MyWeb`) dan jalankan:

```bash
# Inisialisasi git repository
git init

# Tambahkan semua file ke staging
git add .

# Buat commit pertama
git commit -m "Initial commit: Personal website portfolio"
```

### **Langkah 3: Hubungkan dengan GitHub**
Setelah membuat repository di GitHub, Anda akan melihat URL repository. Contoh:
- `https://github.com/username/MyWeb.git`

Jalankan command berikut (ganti dengan URL repository Anda):

```bash
# Tambahkan remote repository
git remote add origin https://github.com/username/MyWeb.git

# Cek apakah remote sudah terhubung
git remote -v
```

### **Langkah 4: Push ke GitHub**
```bash
# Push ke branch main/master
git branch -M main
git push -u origin main
```

Jika menggunakan branch master:
```bash
git push -u origin master
```

---

## 🔐 Jika Diminta Login

### **Opsi 1: Personal Access Token (Recommended)**
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token (classic)
3. Beri nama token, centang scope `repo`
4. Copy token yang dihasilkan
5. Saat push, gunakan token sebagai password (username tetap username GitHub Anda)

### **Opsi 2: GitHub CLI**
```bash
# Install GitHub CLI (jika belum)
# Lalu login
gh auth login
```

### **Opsi 3: SSH Key (Untuk penggunaan jangka panjang)**
Lebih aman dan tidak perlu login setiap kali. Lihat dokumentasi GitHub untuk setup SSH key.

---

## 📝 Command Lengkap (Copy-Paste Ready)

```bash
# 1. Inisialisasi
git init

# 2. Tambahkan semua file
git add .

# 3. Commit
git commit -m "Initial commit: Personal website portfolio"

# 4. Tambahkan remote (GANTI dengan URL repository Anda)
git remote add origin https://github.com/USERNAME/REPO-NAME.git

# 5. Push
git branch -M main
git push -u origin main
```

---

## 🔄 Update Project (Setelah Push Pertama)

Setelah perubahan, jalankan:

```bash
git add .
git commit -m "Deskripsi perubahan Anda"
git push
```

---

## ❓ Troubleshooting

### **Error: "remote origin already exists"**
```bash
git remote remove origin
git remote add origin https://github.com/USERNAME/REPO-NAME.git
```

### **Error: "failed to push some refs"**
```bash
git pull origin main --allow-unrelated-histories
git push -u origin main
```

### **Lupa URL repository?**
```bash
git remote -v
```

---

## 💡 Tips

1. **Buat .gitignore** untuk file yang tidak perlu di-upload:
   ```
   # Tambahkan di .gitignore
   *.log
   .DS_Store
   node_modules/
   ```

2. **Commit message yang baik**:
   - "Add profile photos"
   - "Update contact information"
   - "Fix responsive design"

3. **Jangan commit file sensitif**:
   - Jangan commit password, API keys, atau data pribadi

---

**Selamat! Website Anda sekarang sudah di GitHub! 🎉**
