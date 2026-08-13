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

