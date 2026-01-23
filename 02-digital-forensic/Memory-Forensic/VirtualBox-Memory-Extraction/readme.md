# Virtual Box Memory Extraction

Kali ini saya akan mencoba mengekstraksi memory (RAM) VM Windows yang berjalan pada VirtualBox dan langsung bisa dianalisis melalui tools memory forensic seperti Volatility. Sebenarnya caranya sangat mudah sekali karena ini merupakan salah satu fitur debug yang sudah tersedia default di VirtualBox.

### Langkah-langkah

- Pertama, tentunya VM yang ingin diekstraksi memory nya harus sudah berjalan atau jika untuk tujuan belajar dan simulasi bisa jalankan terlebih dahulu VM Windows / Linux lalu lakukan apa saja di dalamnya untuk menambah artefak forensik, Disini saya menggunakan VM Windows 10.

- Kedua, masuk ke terminal dan jalankan perintah 

```bash
vboxmanage debugvm "<nama_vm>" dumpvmcore --filename <nama_output>

contoh :

vboxmanage debugvm "Windows" dumpvmcore --filename win10_memory.mem
```
- Proses akan memakan waktu tergantung ukuran memory yang di ekstraksi

- Jika sudah maka hasil output sudah siap untuk di analisis