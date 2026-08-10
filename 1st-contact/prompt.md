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

