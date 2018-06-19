<h1>Install WSL<br>(Windows Subsystem for LaTeX eh Linux :)</h1>

<img src="pictures/aen.jpg" width="150">

**AWAS!**

* Penginstallan WSL (Windows Subsystem For L*) memerlukan data Internet beberapa ratus Mega Bytes!
  Jangan dilakukan jika memiliki kuota data Internet terbatas!

* Jika anda **BUKAN** pakar Windows 10; sebaiknya membuat USER baru di Windows 10 untuk mencoba WSL.
  Jika terjadi hal yang tidak diinginkan, anda tinggal menghapus **USER** Windows tersebut, lalu
  mencoba lagi dengan **USER** baru.

* Lakukan penginstallan hingga tuntas! 
  Pembatalan **INSTALL** ditengah jalan dapat berakibat masalah pada penginstallan berikutnya, 
  karena sisa-sisa penginstallan sebelumnya!

* WSL hanya dapat diaktifkan pada Windows 10 versi 1607 (2016) keatas. 
  Informasi versi tersebut didapatkan dengan mencari "About Your PC" (Setting->System->About).

<img src="pictures/wslp10.png" width="800">

Pengaktifan WSL dilakukan melalui PowerShell (admin) dengan mengetikkan:

```PS
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<img src="pictures/wsl01.png"  width="800">

Selanjutnya, silakan restart komputer.

<img src="pictures/wsl02.png"  width="800">

Jika pertama kali, seharusnya belum ada "bash" dalam sistem.
Untuk -- jaga-jaga -- silakan test apakah sudah terdapat "bash" (yang seharusnya tidak).

<img src="pictures/wsl06.png"  width="800">

Melalui Microsoft Store, silakan **INSTALL APPS** yaitu **UBUNTU** (sekitar 200MB).

<img src="pictures/wsl04.png"  width="800">

<img src="pictures/wslp01.png" width="800">

Setelah install, lalu LAUNCH.

<img src="pictures/wsl05.png"  width="800">

Tunggu beberapa menit...

<img src="pictures/wsl07.png"  width="800">

Setelah sukses menginstall, setup "akun" dan "password" sesuai dengan keyakinan dan kepercayaan masing-masing.
Contohnya, di sini akan menggunakan akun bernama "dummy".

<img src="pictures/wslp02.png" width="800">

- - -

UBUNTU siap untuk digunakan!

Melalui PowerShell (non admin) ketikkan:

```PS
bash
```

Langkah pertama ialah meng-update UBUNTU dengan cara:

```bash
sudo su -
```

(menjadi superuser)

```bash
apt-get update
apt-get dist-upgrade -y
apt-get autoremove -y
apt-get autoclean -y

```

<img src="pictures/wsl10.png"  width="800">

OK di-install.

<img src="pictures/wsl11.png"  width="800">

<img src="pictures/wslp06.png" width="800">

Langkah terakhir ialah menginstall paket (sebagai superuser) yang terkait dengan LaTeX.
**AWAS**, ukuran total lebih dari 1 GigaByte!

```BASH
DEBPKG="
aptitude
biber
build-essential
fcitx
fcitx-pinyin
fonts-hack-otf
fonts-hack-ttf
fonts-hack-web
fonts-noto
fonts-noto-cjk
fonts-noto-hinted
fonts-noto-mono
fonts-noto-unhinted
gawk
git
gnome-terminal
gnupg
groff
guake
latexmk
ntfs-3g
perl-doc
rsync
texlive-fonts-recommended
texlive-latex-base
texlive-latex-extra
texlive-latex-recommended
usbutils
vim
wget
whiptail
xfce4
xfce4-terminal
xzdec
"
```

```BASH
apt-get install $DEBPKG
```

<img src="pictures/wslp08.png" width="800">

<img src="pictures/wslp09.png" width="800">

## DISKLAIMER

Tulisan ini terutama untuk <b>KEPERLUAN SENDIRI</b> ---berbasis 
"<i>Google Sana, Google Sini, Coba Itu, Coba Ini, Lalu Tanya-tanyi</i>".
Entah ini <b>PLAGIAT</b>, entah ini <b>RISET</b>, yang jelas tidak pernah ada klaim bahwa ini merupakan karya asli, 
dan belum tentu pula merupakan solusi terbaik :).
Mohon kiranya memberikan tanggapan, terutama jika memiliki solusi alternatif.
Semoga ini bermanfaat di masa mendatang, saat sudah lupa cara menyelesaikan masalah trivia ini.

<a href="http://rahmatm.samik-ibrahim.vlsm.org">Rahmat M. Samik-Ibrahim, revisi 
07--19-Jun-2018</a>
