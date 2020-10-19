# cpuminer-multi-arm-x64
cpuminer multi algorithms for arm x64 and all ready compiled. Forked from cpuminer-multi by tpruvot
CARA MINING CRYPTO CURENCY MENGGUNAKAN HP ANDROID

assalamualaikum warohmatullohi wabarokatuh
halo teman teman sekalian……
pada kesempatan kali ini saya akan memberikan tutorial bagaimana cara menambang crypto curency khusus nya menggunakan hp android.
silahkan ikuti langkah langkah di bawah ini agar proses nya berjalan dengan lancar ya kawan kawan….
1. Install aplikasi termux terlebih dahulu dari google playstore
2. Buka aplikasi termux dan instal beberapa package atau modul untuk termux nya, lalu copy dan paste list command di bawah ini ke aplikasi termux dan jangan lupa tekan enter.
							↓↓↓↓↓↓↓
     		pkg update && pkg upgrade && pkg install -y root-repo unstable-repo x11 repo git wget nano
3. Install 2 buah ubuntu di aplikasi termux.
							↓↓↓↓↓↓↓
			cd && pkg install wget openssl-tool proot -y && hash -r && wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Installer/Ubuntu/ubuntu.sh && bash ubuntu.sh
	lalu buka session baru di termux ya untuk ubuntu yang ke 2
							↓↓↓↓↓↓↓
			cd && git clone https://github.com/kanxck/untumu && cd untumu && chmod 777 ubuntu.sh && ./ubuntu.sh && mv startubuntu.sh /data/data/com.termux/files/home && cd && ls && ./startubuntu.sh
4. Lalu update dan upgrade ubuntu yang di session ke 2 dengan command dibawah ini yang sudah di otomatisasi dengan tambahan instalasi modul ya temsn teman.
							↓↓↓↓↓↓↓
			apt-get update && apt-get upgrade && apt instal -y git wget nano
5. Lalu edit file syslog.h dengan ubuntu yang tadi.
							↓↓↓↓↓↓↓
			nano ../usr/include/syslog.h
	Lalu copy dan paste text dibawah ini ke nano editor di ubuntu yang tadi dibuka gaes
							↓↓↓↓↓↓↓
				#include <sys/syslog.h>
				__android_log_vprint
				__android_log_print
				android_polyfill_vsyslog

   Kemudian untuk menyimpan file, tekan CTRL X Y dan tekan enter

6. Instal modul requirement mining nya
							↓↓↓↓↓↓↓
		apt-get install automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev zlib1g-dev make g++

7. download miner nya pake termux ubuntu
							↓↓↓↓↓↓↓
	wget https://github.com/maribun20/cpuminer-multi-arm-x64/releases/download/cpuminer-multi_arm_x64/cpuminer-multi-arm_v8-x64.tar.gz

8. ekstrak file nya
							 ↓↓↓↓↓↓↓
	chmod +x  cpuminer-multi-arm_v8-x64.tar.gz
	tar xf cpuminer-multi-arm_v8-x64.tar.gz

9. start mining.
							 ↓↓↓↓↓↓↓
	cd cpuminer-multi-arm_v8-x64
	chmod +x cpuminer
	./cpuminer -a yescrypt -o stratum+tcp://yescrypt.sea.mine.zpool.ca:6233 -u wallet-doge-agan -p c=DOGE,zap=BSTY -t 4

10. check earning

       buka https://zpool.ca/wallet
       masukan wallet yang buat mining tadi dan tekan search
       
selamat mencoba dan koin akan masuk ke wallet tiap hari secara otomatis min 0.01 untuk semua koin.
