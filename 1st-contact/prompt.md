*whoami - mengetahui siapa user yang sedang menjalankan command

*hostname - identitas mesin di jaringan.

*cat /etc/os-release - perintah untuk melihat identitas, nama, dan versi Linux yang sedang berjalan.
			   - cat - singkatan dari concatenate. Salah satu penggunaan paling sederhananya adalah membaca dan menampilkan isi file ke terminal.
			   - /etc/os-release - file standar di Linux yang berisi identitas dan informasi versi distribusi Linux.

*uname -r - menampilkan versi kernel Linux yang sedang digunakan.


# OS dan kernel bukan hal yang sama :
		 Debian 12
  			 │
   			 └── menggunakan Linux kernel
            		 │
             		 └── 6.1.0-52-amd64

# cat /etc/os-release menjawab "Saya menggunakan Ubuntu versi berapa?", uname -r menjawab "Saya sedang menjalankan kernel versi berapa?".

*ip addr / ip a - melihat network interface dan alamat IP pada Linux.
			- lo — loopback - interface internal untuk komunikasi mesin dengan dirinya sendiri.
			- enp0s3 — interface jaringan utama.

			 VirtualBox
                 │
                NAT
                 │
          ┌──────┴──────┐
          │             │
       Network        Internet
          │
     enp0s3
     10.0.2.15/24
          │
   ┌──────┴─────────┐
   │                │
Debian 12       Server kita

lo
└── 127.0.0.1
    └── dirinya sendiri

*ip route - untuk melihat routing table Linux — yaitu aturan yang menentukan paket jaringan harus dikirim ke mana.

*ping -c 4 10.0.2.2 - ping gateway
*ping -c 4 1.1.1.1 - ping internet
*ping -c 4 debian.org - ping DNS
            - ping → mengirim paket ICMP untuk mengecek apakah host dapat dijangkau.
            - -c 4 → mengirim 4 paket saja, lalu berhenti.
            - 10.0.2.2 → alamat IP tujuan.

Interface
   │
   ▼
10.0.2.15              ✅
   │
   ▼
Gateway 10.0.2.2       ✅
   │
   ▼
Internet / 1.1.1.1     ✅
   │
   ▼
DNS → debian.org       ✅

# ping DNS penting karena bisa akses IP belum tentu bisa menerjemahkan nama domain.

*free -h - melihat penggunaan RAM (memori) dan swap pada Linux.
         - free → menampilkan informasi penggunaan memori.
         - -h (human-readable) → membuat ukuran lebih mudah dibaca, misalnya Mi, Gi, bukan angka dalam byte.

*lscpu - menampilkan informasi tentang CPU/prosesor pada sistem Linux.

*lsblk - melihat daftar perangkat penyimpanan (storage) dan partisinya di Linux.