# Privilege Management

*apt update - memperbarui daftar informasi paket yang tersedia di sistem Linux berbasis Debian/Ubuntu.

*apt install sudo - menginstal program sudo ke sistem Linux.

*usermod -aG sudo sysadm - menambahkan user sysadm ke grup sudo.
						 - usermod → mengubah konfigurasi user.
						 - -a → append, jadi tidak menghapus grup lain yang sudah dimiliki user.
						 - -G sudo → menambahkan ke grup sudo.
						 - sysadm → nama user yang ditambahkan.

*exit - keluar dari shell/terminal yang sedang aktif. 
	#Contohnya, kalau kamu sedang login sebagai root:
	#exit
	#maka kamu keluar dari sesi root dan kembali ke user sebelumnya, atau jika itu sesi SSH terakhir, koneksi SSH akan terputus.

*id -  melihat identitas dan grup user yang sedang aktif di Linux.

*sudo -l - melihat perintah apa saja yang boleh dijalankan oleh user menggunakan sudo.



# Package Management

*apt list --upgradable - menampilkan paket yang tersedia untuk upgrade, tidak melakukan upgrade.

*sudo apt upgrade - memasang versi paket yang lebih baru.



		# Change → Verify → Confirm.

gunakan apt list --upgradable untuk verify

apt update
    ↓
cek paket upgradable
    ↓
apt upgrade
    ↓
verifikasi
    ↓
0 paket tertinggal ✅


*apt search openssh-server - mencari paket bernama openssh-server di repository APT / hanya melakukan pencarian di database paket dan tidak menginstal apa pun.
	- apt → pengelola paket.
	- search → mencari paket berdasarkan nama/deskripsi.
	- openssh-server → paket yang menyediakan SSH server (sshd).

*sudo apt install openssh-server - untuk menginstal SSH Server di Linux berbasis Debian/Ubuntu.
	- sudo → menjalankan perintah sebagai administrator.
	- apt install → menginstal paket.
	- openssh-server → paket OpenSSH Server, yang menyediakan layanan sshd.


# Service Management    ### Package ≠ Service

*sudo systemctl status ssh - untuk mengecek kondisi/status layanan SSH Server di Linux.
	- sudo → menjalankan dengan hak administrator.
	- systemctl → mengelola service/systemd.
	- status → melihat status service.
	- ssh → service SSH Server.

	#Ada dua status penting di sini:
		- active (running) → service SSH sedang berjalan sekarang.
		- enabled → service akan otomatis dijalankan saat boot.

*ssh localhost - digunakan untuk mencoba koneksi SSH ke komputer itu sendiri.
	- ssh → menjalankan client SSH.
	- localhost → menunjuk ke komputer sendiri (127.0.0.1).

*exit - keluar dari koneksi
