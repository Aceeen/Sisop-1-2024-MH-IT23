# Sisop-1-2024-MH-IT23
# Sisop-1-2024-MH-IT23

## Anggota Kelompok

| NRP        | Nama                            |
|:----------:|:-------------------------------:|
| 5027231020 | Acintya Edria Sudarsono         |
| 5027231044 | Dionisius Marcell Putra Indranto|
| 5027231072 | Aisyah Rahmasari                |

- [Peraturan](#peraturan) 
- [Soal](#soal)
- [Detail Tambahan](#detail-tambahan)
- [Penjelasan](#penjelasan)
  - [Soal 1](#soal-1)
  - [Soal 2](#soal-2)
  - [Soal 3](#soal-3)
  - [Soal 4](#soal-4)
 
## Peraturan
1. Waktu pengerjaan dimulai hari Rabu (20 Maret 2024) setelah sesi lab hingga hari Senin (25 Maret 2024) pukul 23.59 WIB.
2. Praktikan diharapkan membuat laporan penjelasan dan penyelesaian soal dalam bentuk Readme(github).
3. Format nama repository github “Sisop-[Nomor Modul]-2024-[Kode Dosen Kelas]-[Nama Kelompok]” (contoh:Sisop-1-2024-MH-IT01).
4. Struktur repository seperti berikut:
	- soal_1:
		- sandbox.sh
	- soal_2:
		- login.sh
		- register.sh
	- soal_3:
		- awal.sh
		- search.sh
	- soal_4:
		- aggregate_minutes_to_hourly_log.sh
		- minute_log.sh
Jika melanggar struktur repo akan dianggap sama dengan curang dan menerima konsekuensi sama dengan melakukan kecurangan.
5. Setelah pengerjaan selesai, semua script bash, awk, dan file yang berisi cron job ditaruh di github masing - masing kelompok, dan link github diletakkan pada form yang disediakan. Pastikan github di setting ke publik.
6. Commit terakhir maksimal 10 menit setelah waktu pengerjaan berakhir. Jika melewati maka akan dinilai berdasarkan commit terakhir.
7. Jika tidak ada pengumuman perubahan soal oleh asisten, maka soal dianggap dapat diselesaikan.
8. Jika ditemukan soal yang tidak dapat diselesaikan, harap menuliskannya pada Readme beserta permasalahan yang ditemukan.
9. Praktikan tidak diperbolehkan menanyakan jawaban dari soal yang diberikan kepada asisten maupun praktikan dari kelompok lainnya.
10. Jika ditemukan indikasi kecurangan dalam bentuk apapun di pengerjaan soal shift, maka nilai dianggap 0.
11. Pengerjaan soal shift sesuai dengan modul yang telah diajarkan.
12. Zip dari repository dikirim ke email asisten penguji dengan subjek yang sama dengan nama judul repository, dikirim sebelum deadline dari soal shift.
13. Jika terdapat revisi soal akan dituliskan pada halaman terakhir.

## Soal

1. Cipung dan abe ingin mendirikan sebuah toko bernama “SandBox”, sedangkan kamu adalah manajer penjualan yang ditunjuk oleh Cipung dan Abe untuk melakukan pelaporan penjualan dan strategi penjualan kedepannya yang akan dilakukan.

Setiap tahun Cipung dan Abe akan mengadakan rapat dengan kamu untuk mengetahui laporan dan strategi penjualan dari “SandBox”. Buatlah beberapa kesimpulan dari data penjualan “Sandbox.csv” untuk diberikan ke cipung dan abe 

- Karena Cipung dan Abe baik hati, mereka ingin memberikan hadiah kepada customer yang telah belanja banyak. Tampilkan nama pembeli dengan total sales paling tinggi
- Karena karena Cipung dan Abe ingin mengefisienkan penjualannya, mereka ingin merencanakan strategi penjualan untuk customer segment yang memiliki profit paling kecil. 
Tampilkan customer segment yang memiliki profit paling kecil
- Cipung dan Abe hanya akan membeli stok barang yang menghasilkan profit paling tinggi agar efisien. Tampilkan 3 category yang memiliki total profit paling tinggi 
- Karena ada seseorang yang lapor kepada Cipung dan Abe bahwa pesanannya tidak kunjung sampai, maka mereka ingin mengecek apakah pesanan itu ada. Cari purchase date dan amount (quantity) dari nama adriaens

2. Oppie merupakan seorang peneliti bom atom, ia ingin merekrut banyak peneliti lain untuk mengerjakan proyek bom atom nya, Oppie memiliki racikan bom atom rahasia yang hanya bisa diakses penelitinya yang akan diidentifikasi sebagai user, Oppie juga memiliki admin yang bertugas untuk memanajemen peneliti,  bantulah oppie untuk membuat program yang akan memudahkan tugasnya
- Buatlah 2 program yaitu login.sh dan register.sh
- Setiap admin maupun user harus melakukan register terlebih dahulu menggunakan email, username, pertanyaan keamanan dan jawaban, dan password
- Username yang dibuat bebas, namun email bersifat unique. setiap email yang mengandung kata admin akan dikategorikan menjadi admin 
- Karena resep bom atom ini sangat rahasia Oppie ingin password nya memuat keamanan tingkat tinggi
  	- Password tersebut harus di encrypt menggunakan base64
	- Password yang dibuat harus lebih dari 8 karakter
	- Harus terdapat paling sedikit 1 huruf kapital dan 1 huruf kecil
	- Harus terdapat paling sedikit 1 angka 
- Karena Oppie akan memiliki banyak peneliti dan admin ia berniat untuk menyimpan seluruh data register yang ia lakukan ke dalam folder users file users.txt. Di dalam file tersebut, terdapat catatan seluruh email, username, pertanyaan keamanan dan jawaban, dan password hash yang telah ia buat.
- Setelah melakukan register, program harus bisa melakukan login. Login hanya perlu dilakukan menggunakan email dan password.
- Karena peneliti yang di rekrut oleh Oppie banyak yang sudah tua dan pelupa maka Oppie ingin ketika login akan ada pilihan lupa password dan akan keluar pertanyaan keamanan dan ketika dijawab dengan benar bisa memunculkan password
- Setelah user melakukan login akan keluar pesan sukses, namun setelah seorang admin melakukan login Oppie ingin agar admin bisa menambah, mengedit (username, pertanyaan keamanan dan jawaban, dan password), dan menghapus user untuk memudahkan kerjanya sebagai admin. 
- Ketika admin ingin melakukan edit atau hapus user, maka akan keluar input email untuk identifikasi user yang akan di hapus atau di edit
- Oppie ingin programnya tercatat dengan baik, maka buatlah agar program bisa mencatat seluruh log ke dalam folder users file auth.log, baik login ataupun register.
  	- Format: [date] [type] [message]
	- Type: REGISTER SUCCESS, REGISTER FAILED, LOGIN SUCCESS, LOGIN FAILED
	- Ex:
	  	- [23/09/17 13:18:02] [REGISTER SUCCESS] user [username] registered successfully
		- [23/09/17 13:22:41] [LOGIN FAILED] ERROR Failed login attempt on user with email [email]
3. Alyss adalah seorang gamer yang sangat menyukai bermain game Genshin Impact. Karena hobinya, dia ingin mengoleksi foto-foto karakter Genshin Impact. Suatu saat Yanuar memberikannya sebuah Link yang berisi koleksi kumpulan foto karakter dan sebuah clue yang mengarah ke penemuan gambar rahasia. Ternyata setiap nama file telah dienkripsi dengan menggunakan hexadecimal. Karena penasaran dengan apa yang dikatakan Yanuar, Alyss tidak menyerah dan mencoba untuk mengembalikan nama file tersebut kembali seperti semula.
- Alyss membuat script bernama awal.sh, untuk download file yang diberikan oleh Yanuar dan unzip terhadap file yang telah diunduh dan decode setiap nama file yang terenkripsi dengan hex . Karena pada file list_character.csv terdapat data lengkap karakter, Alyss ingin merename setiap file berdasarkan file tersebut. Agar semakin rapi, Alyss mengumpulkan setiap file ke dalam folder berdasarkan region tiap karakter
	- Format: Region - Nama - Elemen - Senjata.jpg
- Karena tidak mengetahui jumlah pengguna dari tiap senjata yang ada di folder "genshin_character".Alyss berniat untuk menghitung serta menampilkan jumlah pengguna untuk setiap senjata yang ada
   	- Format: [Nama Senjata] : [jumlah]
   	  Untuk menghemat penyimpanan. Alyss menghapus file - file yang tidak ia gunakan, yaitu genshin_character.zip, list_character.csv, dan genshin.zip
- Namun sampai titik ini Alyss masih belum menemukan clue dari the secret picture yang disinggung oleh Yanuar. Dia berpikir keras untuk menemukan pesan tersembunyi tersebut. Alyss membuat script baru bernama search.sh untuk melakukan pengecekan terhadap setiap file tiap 1 detik. Pengecekan dilakukan dengan cara meng-ekstrak sebuah value dari setiap gambar dengan menggunakan command steghide. Dalam setiap gambar tersebut, terdapat sebuah file txt yang berisi string. Alyss kemudian mulai melakukan dekripsi dengan hex pada tiap file txt dan mendapatkan sebuah url. Setelah mendapatkan url yang ia cari, Alyss akan langsung menghentikan program search.sh serta mendownload file berdasarkan url yang didapatkan.
- Dalam prosesnya, setiap kali Alyss melakukan ekstraksi dan ternyata hasil ekstraksi bukan yang ia inginkan, maka ia akan langsung menghapus file txt tersebut. Namun, jika itu merupakan file txt yang dicari, maka ia akan menyimpan hasil dekripsi-nya bukan hasil ekstraksi. Selain itu juga, Alyss melakukan pencatatan log pada file image.log untuk setiap pengecekan gambar
	- Format: [date] [type] [image_path]
   	- Ex:
   	  	- [24/03/20 17:18:19] [NOT FOUND] [image_path]
   	  	- [24/03/20 17:18:20] [FOUND] [image_path]
- Hasil akhir:
	- genshin_character
	- search.sh
	- awal.sh
	- image.log
	- [filename].txt
	- [image].jpg
4. Stitch sangat senang dengan PC di rumahnya. Suatu hari, PC nya secara tiba-tiba nge-freeze 🤯 Tentu saja, Stitch adalah seorang streamer yang harus setiap hari harus bermain game dan streaming.  Akhirnya, dia membawa PC nya ke tukang servis untuk diperbaiki. Setelah selesai diperbaiki, ternyata biaya perbaikan sangat mahal sehingga dia harus menggunakan uang hasil tabungan nya untuk membayarnya. Menurut tukang servis, masalahnya adalah pada CPU dan GPU yang overload karena gaming dan streaming sehingga mengakibatkan freeze pada PC nya. Agar masalah ini tidak terulang kembali, Stitch meminta kamu untuk membuat sebuah program monitoring resource yang tersedia pada komputer.
Buatlah program monitoring resource pada PC kalian. Cukup monitoring ram dan monitoring size suatu directory. Untuk ram gunakan command `free -m`. Untuk disk gunakan command `du -sh <target_path>`. Catat semua metrics yang didapatkan dari hasil `free -m`. Untuk hasil `du -sh <target_path>` catat size dari path directory tersebut. Untuk target_path yang akan dimonitor adalah /home/{user}/.
- Masukkan semua metrics ke dalam suatu file log bernama metrics_{YmdHms}.log. {YmdHms} adalah waktu disaat file script bash kalian dijalankan. Misal dijalankan pada 2024-03-20 15:00:00, maka file log yang akan tergenerate adalah metrics_20240320150000.log.
- Script untuk mencatat metrics diatas diharapkan dapat berjalan otomatis pada setiap menit.
- Kemudian, buat satu script untuk membuat agregasi file log ke satuan jam. Script agregasi akan memiliki info dari file-file yang tergenerate tiap menit. Dalam hasil file agregasi tersebut, terdapat nilai minimum, maximum, dan rata-rata dari tiap-tiap metrics. File agregasi akan ditrigger untuk dijalankan setiap jam secara otomatis. Berikut contoh nama file hasil agregasi metrics_agg_2024032015.log dengan format metrics_agg_{YmdH}.log
- Karena file log bersifat sensitif pastikan semua file log hanya dapat dibaca oleh user pemilik file.
Note:
- Nama file untuk script per menit adalah minute_log.sh
- Nama file untuk script agregasi per jam adalah aggregate_minutes_to_hourly_log.shN
- Semua file log terletak di /home/{user}/log
- Semua konfigurasi cron dapat ditaruh di file skrip .sh nya masing-masing dalam bentuk comment
Berikut adalah contoh isi dari file metrics yang dijalankan tiap menit:
mem_total,mem_used,mem_free,mem_shared,mem_buff,mem_available,swap_total,swap_used,swap_free,path,path_size 15949,10067,308,588,5573,4974,2047,43,2004,/home/user/coba/,74M
Berikut adalah contoh isi dari file aggregasi yang dijalankan tiap jam:
type,mem_total,mem_used,mem_free,mem_shared,mem_buff,mem_available,swap_total,swap_used,swap_free,path,path_size minimum,15949,10067,223,588,5339,4626,2047,43,1995,/home/user/coba/,50M maximum,15949,10387,308,622,5573,4974,2047,52,2004,/home/user/coba/,74M average,15949,10227,265.5,605,5456,4800,2047,47.5,1999.5,/home/user/coba/,62M

## Detail Tambahan
Tidak ada penambahan detail mengenai soal yang diberikan

## Penjelasan

### SOAL 1
a. Tampilkan nama pembeli dengan total sales paling tinggi <br />
 	`awk -F ',' 'NR == 1 { next } { if ($17 > tertinggi) { tertinggi = $17; cust = $6 } } END { print cust }' Sandbox.csv` <br />
 	command ini melangkahi baris header dengan NR == 1 {next} dan membandingkan nilai sales di kolom 17 berdasarkan nama customer di kolom 6. <br /> <br />
b. Tampilkan customer segment yang memiliki profit paling kecil <br />
	`profitMin=$(awk -F ',' 'NR > 1 { segment[$14] += $NF; if (minProfit == "" || segment[$14] < minProfit) { minProfit = segment[$14]; minSegment = $14 } } END { print minSegment }' Sandbox.csv)` <br />
 	line _if (minProfit == "" || segment[$14] < minProfit)_ akan terus membandingkan total profit dari kolom $NF atau kolom terakhir dengan minProfit hingga didapat profit terkecil. <br /> <br />
c. Tampilkan 3 category yang memiliki total profit paling tinggi <br />
	`awk -F ',' '{sum[$14] += $20} END { for (Category in sum) { print Category } }' Sandbox.csv | sort -nr | head -n 3` <br />
 	line _{sum[$14] += $20}_ akan menjumlahkan nilai di kolom 20 dengan menggunakan kategori di kolom 14 sebagai identifier <br />
  	line _sort -nr | head -n 3_ akan rearrange order dari highest to lowest dan hanya mengoutput 3 teratas. <br /> <br />
d. Cari purchase date dan amount (quantity) dari nama adriaens <br />
	`awk -F ',' 'NR==1 { for (i=1; i<=NF; ++i) headers[i] = $i; next } { if ($6 == "Adriaens Grayland") { print headers[2], $2, headers[18], $18 } }' Sandbox.csv` <br />
 	jika pada kolom 6 ditemukan "Adriaens Grayland" maka kolom 2 dan 18 pada baris yang sama dengan baris ditemukan Adriaens akan di print. <br />
  	Terakhir gabungkan ke dalam 1 script <br />

   	`
    	#!/bin/bash

	# Sales terbanyak
	sales_terbanyak=$(awk -F ',' 'NR == 1 { next } { if ($17 > tertinggi) { tertinggi = $17; cust = $6 } } END { print cust }' Sandbox.csv)
	
	# Segment dengan profit terkecil
	profitMin=$(awk -F ',' 'NR > 1 { segment[$14] += $NF; if (minProfit == "" || segment[$14] < minProfit) { minProfit = segment[$14]; minSegment = $14 } } END { print minSegment }' Sandbox.csv)
	
	# 3 kategori dengan profit terbanyak
	top3cat=$(awk -F ',' '{sum[$14] += $20} END { for (Category in sum) { print Category } }' Sandbox.csv | sort -nr | head -n 3)
	
	# Order date dan quantity dari pemesanan Adriaens
	adriaens=$(awk -F ',' 'NR==1 { for (i=1; i<=NF; ++i) headers[i] = $i; next } { if ($6 == "Adriaens Grayland") { print headers[2], $2, headers[18], $18 } }' Sandbox.csv)
	
	# Print results
	echo "Sales terbanyak: $sales_terbanyak"
	echo "Segment dengan profit terkecil: $profitMin"
	echo "Top 3 Categories: $top3cat"
	echo "Adriaens order date dan quantity:"
	echo "$adriaens"
    	
    	`
### SOAL 2
-Aisyah Rahmasari (5027231072)

Berikut adalah tugas untuk membuat sebuah program untuk manajemen registrasi dan login sistem dengan beberapa fitur:
- Registrasi:
Pengguna harus mendaftar menggunakan email, username, pertanyaan keamanan, jawaban keamanan, dan password.
Informasi setiap akun akan disimpan dalam sebuah file bernama users.txt.
- Login:
Pengguna memiliki opsi untuk login atau mengatasi lupa password.
- Opsi Lupa Password:
Jika pengguna lupa password, mereka dapat menggunakan pertanyaan keamanan untuk meresetnya.
- Fitur Admin:
Jika login sebagai admin, akan muncul menu admin dengan opsi untuk menambah, mengedit, atau menghapus pengguna. Opsi untuk logout juga akan tersedia.
- Rekaman Aktivitas:
Semua registrasi dan login akan direkam ke dalam sebuah file bernama auth.log.

## Membuat menu Register

1. Pertama - tama kita perlu membuat function untuk memeriksa apakah email yang dimasukkan telah terdaftar, mengecek apakah email tersebut sudah ada dalam file users.txt, serta mengembalikan nilai 0 jika email ditemukan, dan 1 jika tidak ditemukan.

```sh
#!/bin/bash
#Function to check if email is already registered
function check_email() {
  local email="$1"
  if grep -q "^$email:" users.txt; then
    return 0  # Email found
  else
    return 1  # Email not found
  fi
}
```

2. Lalu, fungsi ini bertujuan untuk mengenkripsi password menggunakan base64, menerima satu parameter, yaitu password yang ingin dienkripsi, menggunakan perintah base64 untuk melakukan enkripsi.

```sh
#Function to encrypt password 
function encrypt_password() {
  echo -n "$1" | base64
}
```

3. Membuat function untuk membuat akun baru yang dimana fungsi ini menerima beberapa argumen, yaitu alamat email, username, pertanyaan keamanan, jawaban keamanan, dan password. Variabel user_type membantu membedakan antara pengguna biasa dan pengguna admin dalam sistem.

```sh
#Function to register a new user account
function register() {
  local email="$1"
  local username="$2"
  local security_question="$3"
  local security_answer="$4"
  local password="$5"
  local user_type="user"
```

* Pernyataan if ini memeriksa apakah variabel email sama persis dengan string "admin".Jika email sama dengan "admin", maka nilai variabel user_type diubah menjadi "admin".

```sh
#Check for "admin" in email and set admin flag
    if [[ "$email" == admin ]]; then
        user_type="admin"
    fi
```

* Fungsi check_email melakukan dua tugas utama: Memastikan alamat email yang diberikan memiliki format yang valid dan Mengecek apakah alamat email tersebut sudah terdaftar di dalam sistem.

```sh
#Check if email is already registered
  check_email "$email"
  if [ $? -eq 0 ]; then
    echo "[ $(date +'%d/%m/%Y %H:%M:%S') ] [REGISTER FAILED>  Email $email already registered." >&2
    echo "Email $email already registered." >&2
    exit 1
  fi
```

* Fungsi ini digunakan untuk memvalidasi (memeriksa kesahihan) password yang dimasukkan pengguna menggunakan loop. Validasi memastikan password memenuhi kriteria keamanan minimum untuk melindungi akun dari akses tidak sah.

```sh
#Validate password 
  while true; do 
    read -s -p "Enter password: " password
    echo
    if [[ "$password" =~ [[:upper:]] && "$password" =~ [[:lower:]] && "$password" =~ [[:digit:]] && ${#password} -ge 8 ]]; then
      break
    else
      echo "Password must be at least 8 characters long and  contain at least one uppercase letter, one lowercase letter, and one digit."
      echo "Please try again."
    fi
  done
```

* Password tersebut akan dienkripsi menggunakan function "encrypt_password" dan akan disimpan dalam variabel "encrypted_password"

```sh
  #Encrypt password
  local encrypted_password=$(encrypt_password "$password")
```

* Fungsi yang diberikan berfungsi untuk menulis data pengguna ke dalam file users.txt dengan menambahkan flag admin jika pengguna tersebut adalah seorang administrator. Ini juga mencatat tindakan registrasi pengguna ke dalam file auth.log dengan memberikan pesan yang sesuai.

```sh
  #Write user data to users.txt with admin flag
  echo "$email:$username:$security_question:$security_answer:$encrypted_password:$user_type" >> users.txt

  if [[ $user_type == "admin" ]]; then
    echo "[ $(date +'%d/%m/%Y %H:%M:%S') ] [REGISTER SUCCESS] Admin $username registered successfully." >> auth.log
    echo "Admin $username registered successfully."
  else
    echo "[ $(date +'%d/%m/%Y %H:%M:%S') ] [REGISTER SUCCESS] User $username registered successfully." >> auth.log
    echo "User $username registered successfully."
  fi
}
```

4. Membuat file users.txt jika belum ada lalu meminta pengguna untuk memasukkan data registrasi, termasuk email, username, pertanyaan keamanan, jawaban keamanan, dan password.

```sh
#Main script 
#Create users.txt if it doesnt exist
touch users.txt # add this line to create the file if it doesnt exist
echo "User Registration"
read -p "Enter email: " email
read -p "Enter username: " username
read -p "Enter security question: " security_question
read -p "Enter security answer: " security_answer
read -sp "Password: " password
echo
```

5. Dan akhirnya memanggil fungsi register() untuk menyelesaikan proses registrasi.

```sh
#Call the register function to complete registration
register "$email" "$username" "$security_question" "$security_answer" "$password"
```

### Dokumentasi 
Jika di jalankan maka akan seperti ini : 
![Screenshot 2024-03-30 185729](https://github.com/Aceeen/Sisop-1-2024-MH-IT23/assets/151058945/faaea015-6fab-4045-88eb-b6ca7b12f4f5)

## Membuat menu Login

1. Membuat fungsi untuk memastikan apakah user sudah tersimpan dalam sistem atau belum
   
 * Fungsi ini bertanggung jawab untuk memeriksa apakah pengguna dengan alamat email yang diberikan ada dalam file users.txt dan apakah kata sandi yang diberikan sesuai dengan kata sandi yang terkait dengan alamat email tersebut. Jika tidak ketemu, maka akan kembali ke menu awal

```sh
#!/bin/bash

# Function to check if the user exists or not
function authenticate_user() {
    local email="$1"
    local password="$2"

    # Search for the user in users.txt
    local user_info=$(grep "^$email:" /home/syahrhm/sisop/mod1no2/users.txt)

    # If not found, return to the main menu
    if [ -z "$user_info" ]; then
        echo "User with email $email not found."
        exit 1
    fi
```
* Lalu kode ini bertujuan untuk mengambil kata sandi terenkripsi dari informasi pengguna yang ditemukan dalam file users.txt, lalu mendekripsi kata sandi tersebut menggunakan algoritma enkripsi base64.
  
```sh
    # Retrieve encrypted password information
    local encrypted_password=$(echo "$user_info" | cut -d: -f5)

    # Decrypt the password using base64
    local decrypted_password=$(echo "$encrypted_password" | base64 -d)
```

* Lalu kita harus memeriksa apakah kata sandi yang dimasukkan oleh pengguna saat login sesuai dengan kata sandi yang telah didekripsi dari data pengguna yang tersimpan dalam file users.txt.

```sh
    # Check if the entered password matches the stored password
    if [ "$password" != "$decrypted_password" ]; then
        echo "Incorrect password."
        exit 1
    fi
```

* Saat sudah ingin login, pengguna akan di cek apakah pengguna yang berhasil login adalah seorang admin atau tidak. Jika pengguna bukan seorang admin, maka akan dicetak pesan bahwa pengguna tidak memiliki izin untuk mengakses fitur tertentu, dan kemudian fungsi admin_menu akan dipanggil untuk menampilkan menu admin. Jika pengguna adalah seorang admin, pesan sukses akan dicetak, log login akan dicatat, dan fungsi admin_menu juga akan dipanggil.

```sh
    # Check if the user is an admin, if not, return
    local user_type=$(echo "$user_info" | cut -d: -f6)
    if [ "$user_type" != "admin" ]; then
        echo "You do not have permission to access this feature."
        admin_menu "$email"
	return 0
    fi

    echo "Login successful!"
    echo "$(date '+[%d/%m/%y %H:%M:%S]') [LOGIN SUCCESS] User $email successfully logged in." >> /home/syahrhm/sisop/mod1no2/auth.log
    admin_menu "$email"
    exit 1
}
```
2. Membuat fungsi ketika melupakan password dari pengguna

* Jadi, fungsi forgot_password digunakan untuk mencari alamat email pengguna dalam file users.txt. Jika pengguna dengan alamat email yang diberikan tidak ditemukan, maka fungsi ini akan mengembalikan nilai 1 untuk menunjukkan kegagalan.

```sh
# Function for handling forgotten passwords
function forgot_password() {
    local email="$1"

    # Search for the user in users.txt
    local user_info=$(grep "^$email:" /home/syahrhm/sisop/mod1no2/users.txt)

    # If not found, return to the main menu
    if [ -z "$user_info" ]; then
        echo "User with email $email not found."
        return 1
    fi
```

* Jadi, bagian ini dari fungsi forgot_password bertanggung jawab untuk menampilkan pertanyaan keamanan kepada pengguna dan mengekstrak jawaban keamanan yang telah disimpan sebelumnya dalam data pengguna.

```sh
    # Retrieve security question information
    local security_question=$(echo "$user_info" | cut -d: -f3)

    # Prompt the user to answer the security question
    read -p "Security Question: $security_question " provided_security_answer

    # Retrieve stored security answer
    local stored_security_answer=$(echo "$user_info" | cut -d: -f4)
```

* Dengan demikian, fungsi forgot_password bertindak sebagai mekanisme untuk membantu pengguna yang lupa kata sandi dengan memungkinkan mereka menjawab pertanyaan keamanan yang telah ditetapkan sebelumnya dan mereset kata sandi mereka. Jika tidak maka akan menampilkan "Incorrect answer" dan kembali ke menu awal.
* Jika jawaban keamanannya benar, maka tampilkan kata sandi pengguna yang masih terenkripsi, kemudian dekripsi menggunakan fungsi decrypted_password dan tampilkan hasilnya.

```sh
    # Check if the provided answer matches the stored answer
    if [ "$provided_security_answer" != "$stored_security_answer" ]; then
        echo "Incorrect answer."
        return 1
    fi

    # Retrieve and display the user's password
    local encrypted_password=$(echo "$user_info" | cut -d: -f5)
    local decrypted_password=$(echo "$encrypted_password" | base64 -d)
    echo "Your password is: $decrypted_password"
    return 0
}
```

3. Membuat menu Admin

*Berikut adalah implementasi fungsi admin_menu dalam skrip Bash. Fungsi ini bertujuan untuk menampilkan menu admin yang mencakup opsi untuk menambah, mengedit, atau menghapus pengguna, serta opsi untuk logout. Pengguna akan diminta untuk memilih salah satu opsi yang tersedia menggunakan perintah case. Selama pengguna masih aktif dalam menu admin, fungsi akan terus menampilkan menu dan memproses pilihan yang dibuat pengguna. Loop akan berhenti saat pengguna telah memilih opsi logout.

```sh
# Admin menu function
function admin_menu() {
    local email="$1"
    while true; do
        # Display admin menu options
        echo "Admin Menu"
        echo "1. Add User"
        echo "2. Edit User"
        echo "3. Remove User"
        echo "4. Logout"
        read -p "Choose an option: " admin_option

        case $admin_option in
            1)
                add_user
                ;;
            2)
                read -p "Enter user's email to edit: " edit_email
                edit_user "$edit_email"
                ;;
            3)
                read -p "Enter user's email to remove: " remove_email
                remove_user "$remove_email"
                ;;
            4)
                echo "Logging out..."
                exit 0
                ;;
            *)
                echo "Invalid option. Please choose again."
                ;;
        esac
    done
}

4. Membuat fungsi dari add user, edit user, remove user

* Fungsi add_user akan mengarahkan pengguna ke menu registrasi dengan pesan "Redirecting to the registration menu...".
```sh
# Function to add a new user
function add_user() {
    # Redirect to the registration page
    /home/syahrhm/sisop/mod1no2/register.sh
}
```
* Fungsi edit_user memungkinkan pengguna untuk mengganti username dan password pengguna yang sudah ada dalam file users.txt.

```sh
# Function to edit user information
function edit_user() {
    local email="$1"
    # Input new user information and update users.txt accordingly
    # Example: read -p "Enter new username: " new_username
    #          sed -i "s/^$email:.*/$email:$new_username:/" /home/syahrhm/sisop/mod1no2/data/users.txt
}
```
* Fungsi remove_user memungkinkan pengguna untuk menghapus pengguna yang ada dalam file users.txt. Jika pengguna dengan email yang dimasukkan ditemukan, pengguna akan dihapus dan pesan sukses akan dicetak. Jika tidak, pesan bahwa pengguna tidak ditemukan akan dicetak.

```sh
# Function to remove a user
function remove_user() {
    local email="$1"
    # Remove user from users.txt
    # Example: sed -i "/^$email:/d" /home/syahrhm/sisop/mod1no2/data/users.txt
}
```
5. Main script

* Keseluruhan skrip ini bertujuan untuk memandu pengguna melalui proses masuk atau pemulihan kata sandi, tergantung pada pilihan yang mereka buat. Jika pengguna memilih opsi "login", mereka akan diminta untuk memasukkan alamat email dan kata sandi mereka. Setelah itu, sistem akan menggunakan fungsi authenticate_user untuk memeriksa apakah pengguna sudah terdaftar atau belum.
* Sementara jika pengguna memilih opsi "Forgot Password", mereka akan diminta untuk memasukkan alamat email mereka. Alamat email ini akan diproses melalui fungsi forgot_password untuk menginisiasi proses pemulihan kata sandi.
* Ketika pengguna memilih opsi "login", mereka akan diminta untuk memasukkan alamat email dan kata sandi mereka. Setelah itu, sistem akan menggunakan fungsi authenticate_user untuk memeriksa apakah pengguna sudah terdaftar atau belum.
* Namun, jika pengguna memilih opsi "Forgot Password", mereka akan diminta untuk memasukkan alamat email mereka. Alamat email ini akan diproses melalui fungsi forgot_password untuk memulai proses pemulihan kata sandi.

```sh
# Main script starts here
# Prompt user for login details
echo "Welcome to Login System"
echo "1. Login"
echo "2. Forgot Password"
read -p "Enter your choice: " choice

case $choice in
    1)
        # Login option selected
        read -p "Enter email: " email
        read -s -p "Enter password: " password
        echo
        authenticate_user "$email" "$password"
        ;;
    2)
        # Forgot Password option selected
        read -p "Enter email: " email
        forgot_password "$email"
        ;;
    *)
        echo "Invalid choice. Please select 1 or 2."
        ;;
esac
```

### Dokumentasi ketika menu login di jalankan
* Menjalankan menu login dan login menggunakan user sisopmudah@gmail.com
![Screenshot 2024-03-30 194556](https://github.com/Aceeen/Sisop-1-2024-MH-IT23/assets/151058945/bb37d376-f260-4b0f-aa64-2cb7d8ffa8cd)

* Menjalankan menu login menggunakan user admin-it@gmail.com dan memilih opsi 1 yaitu Add User
![Screenshot 2024-03-30 194635](https://github.com/Aceeen/Sisop-1-2024-MH-IT23/assets/151058945/024ab558-b2e1-4839-b9fd-c89f0e3f5907)

*Memilih opsi 2 dan 3 yaitu Edit User dan Remove User
![Screenshot 2024-03-30 194743](https://github.com/Aceeen/Sisop-1-2024-MH-IT23/assets/151058945/f13f8147-0839-4fef-b570-f42551093ea3)

### REVISI
1. Ketika login menggunakan kata 'admin', maka pengguna admin akan langsung di alihkan ke menu_admin
![Screenshot 2024-03-30 194635](https://github.com/Aceeen/Sisop-1-2024-MH-IT23/assets/151058945/e7364f2b-3953-43c0-8cd9-1f7957b7bad6)

* Berikut perubahan kode skrip untuk menampilkan menu_admin
Sebelum revisi :
```sh
 # Check if the user is an admin, if not, return
    local user_type=$(echo "$user_info" | cut -d: -f6)
    if [ "$user_type" != "admin" ]; then
        echo "You do not have permission to access this feature."
        return 1
    fi

    echo "Login successful!"
    echo "$(date '+[%d/%m/%y %H:%M:%S]') [LOGIN SUCCESS] User $email successfully logged in." >> /home/syahrhm/sisop/mod1no2/auth.log

    admin_menu "$email"

    return 0
}
```

Sesudah revisi :
```sh
 # Check if the user is an admin, if not, return
    local user_type=$(echo "$user_info" | cut -d: -f6)
    if [ "$user_type" != "admin" ]; then
        echo "You do not have permission to access this feature."
        admin_menu "$email"
	return 0
    fi

    echo "Login successful!"
    echo "$(date '+[%d/%m/%y %H:%M:%S]') [LOGIN SUCCESS] User $email successfully logged in." >> /home/syahrhm/sisop/mod1no2/auth.log
    admin_menu "$email"
    exit 1
}
```

### SOAL 3
```sh
#!/bin/bash
wget 'https://drive.google.com/uc?export=download&id=1oGHdTf4_76_RacfmQIV4i7os4sGwa9vN' -O genshin.zip
unzip genshin.zip
unzip genshin_character.zip
```
Kita perlu mendownload file zip dari link yang sudah disediakan lalu melakukan unzip terhadap file-file yang telah didownload
```sh
cd genshin_character
ls | while read -r filename ; do
        decrypted=$(echo "$filename" | xxd -r -p)
        cd ..
        char_atr=$(grep "$decrypted" list_character.csv | sed 's/^[[:space:]]//;s/[[:space:]]$//')
        cd genshin_character
        char_atr=$(echo "$char_atr" | cut -d ',' -f 2-)
        char_elements=$(echo "$char_atr" | cut -d ',' -f 2-| tr ',' '_')
        char_regions=$(echo "$char_atr" | cut -d ',' -f 1)
        newfilename="${char_regions}_${decrypted}_${char_elements}"
        mv "$filename" "${newfilename}.jpg"
        directory="/home/ubuntu/sisop/genshin_character/$char_regions/"
        mkdir -p "$char_regions"
        mv "${newfilename}.jpg" "$char_regions/" 
done
```
Nama dari karakter-karakter yang didapat tersebut dalam kondisi ter-enkripsi dengan base64, maka dilakukan dekripsi dengan memasukkan hasil dekripsi ke variabel decrypted kemudian dilakukan rename nama ‘new file’ menjadi isi dari variabel ‘decrypted'
Setelah mendapatkan nama asli dari setiap karakter, cek file 'list_character.csv' lalu masukkan semua item dari karakter tersebut ke variabel 'attributes', 'elements', 'regions'. Pindahkan dalam folder sesuai region dengan format Nama - Region - Elemen - Senjata
```sh
cd ..

echo "JUMLAH JENIS SENJATA"

tail -n +2 list_character.csv | awk -F ',' '{print $4}' | sed 's/^[[:space:]]//;s/[[:space:]]$//' |  sort | uniq -c | while read -r count word; do
        echo "$word : $count"
done 

rm genshin_character.zip genshin.zip list_character.csv
```
Lalu, lakukan penghitungan terhadap jumlah berbagai jenis senjata yang terdapat di dalam folder lalu remove file 'list_character.csv', 'genshin_character.zip', 'genshin.zip'
## search.sh
```sh
#!/bin/bash

while true; do
  waktu=$(date +"%Y%m%d%H%M%S")

  find genshin_character/ -maxdepth 2 -type f | while read -r file; do
    steghide extract -sf "$file" -p "" -xf extracted.txt
    cat extracted.txt
    decrypted_txt=$(base64 -d extracted.txt)
    echo "$decrypted_txt"
    if [[ $decrypted_txt == https* ]]; then
      wget "$decrypted_txt"
      echo "$decrypted_txt" > decrypted_url.txt
```
Lalu diperlukan script baru yaitu 'search.sh' untuk mencari clue rahasia untuk mendapatkan link gambar. Dilakukan extract dan dekripsi terhadap file-file yang terdapat di dalam 'genshin_character' dan dimasukkan link url tersebut ke dalam 'decrypted_url.txt'
```sh
      rm extracted.txt
      echo "[$waktu] [FOUND] [$file]" >> image.log
      exit 0 
    fi
    echo "[$waktu] [NOT FOUND] [$file]" >> image.log
    rm extracted.txt
  done

  sleep 1

  if [[ $? -eq 0 ]]; then
    break
  fi
done
```
Diperlukan adanya report data ketika kita melaksanakan extract maka dibuat 'image.log' dengan format [date] [type] [image_path], lalu melakukan remove terhadap 'extracted.txt'. Lalu ketika sudah menemukan url dan sudah mendapatkan status FOUND maka script berhenti
