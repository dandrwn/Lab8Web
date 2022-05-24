# Pemograman Web
~~~
Nama    : Dani Darmawan
NIM     : 312010154
KELAS   : TI.20.B1
~~~
# Menjalankan Web Server
Untuk menjalankan web server dari menu XAMPP Control.
![image](https://user-images.githubusercontent.com/101440705/168745921-c68efec2-b2b9-46c2-9935-2366849a64e7.png)

# Memulai PHP
Buat folder lab7_php_dasar pada root directory web server (d:\xampp\htdocs)
![image](https://user-images.githubusercontent.com/101440705/168746210-2b4ab5af-7821-4db8-b749-90d3a083d30f.png)

Kemudia untuk mengakses direktory tersebut pada web server dengan mengakses URL: http://localhost/lab7_php_dasar/ 
![image](https://user-images.githubusercontent.com/101440705/168746360-c344fc56-adf0-4691-ae24-adba0f38414b.png)

# PHP Dasar
Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat kode seperti berikut.
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
~~~
Kemudian untuk mengakses hasilnya melalui URL: http://localhost/lab7_php_dasar/php_dasar.php
![image](https://user-images.githubusercontent.com/101440705/168747289-d65faf1c-9cbf-42a4-95ed-e76a9baa3255.png)

# Variable PHP
Menambahkan variable pada program
~~~
<h2>Menggunakan Variable</h2>
    <?php
        $nim = "311910284";
        $nama = 'Andry Prasetia Perdana';
        echo "NIM : " . $nim . "<br>";
        echo "Nama : $nama";
    ?>
~~~
![image](https://user-images.githubusercontent.com/101440705/168756169-cd66d09c-211f-4a0b-9843-33fccdd69529.png)

# Predefine Variable $_GET
~~~
<h2>Predefine Variable</h2>
    <?php 
        echo 'Selamat Datang ' . $_GET['nama'];
    ?>
~~~
Untuk mengaksesnya gunakan URL: http://localhost/lab7_php_dasar/latihan2.php?nama=Dani
![image](pict/1.jpg) 
![image](pict/redifine.jpg)

# Membuat Form Input
~~~
<h2>Form Input</h2>
    <form method="post">
        <label>Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="Kirim">
    </form>
    <?php 
        echo 'Selamat Datang ' . $_POST['nama'];
    ?>
~~~
![image](pict/2.jpg) 
![image](pict/form.jpg)
# Operator
~~~
<h2>Operator</h2>
    <?php
        $gaji = 1000000;
        $pajak = 0.1;
        $thp = $gaji - ($gaji*$pajak);
            echo "Gaji sebelum pajak = Rp. $gaji <br>";
            echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>
~~~
![image](pict/op1.jpg)
![image](pict/op.jpg)

# Kondisi IF
~~~
<h2>Kondisi IF</h2>
    <?php
        $nama_hari = date("l");
            if ($nama_hari == "Sunday") {
        echo "Minggu";
            } elseif ($nama_hari == "Monday") {
        echo "Senin";
            } else {
        echo "Selasa";
        }
    ?>
~~~
![image](pict/if.jpg)
![image](pict/if1.jpg)


# Kondisi Switch
~~~
<h2>Kondisi Switch</h2>
    <?php
        $nama_hari = date("l");
            switch ($nama_hari) {
            case "Sunday":
        echo "Minggu";
            break;
            case "Monday":
    echo "Senin";
            break;
            case "Tuesday":
    echo "Selasa";
            break;
            default:
    echo "Sabtu";
            }
    ?>
~~~
![image](pict/switch.jpg)

# Perulangan for
~~~
<h2>Perulangan For</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
            for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
        }
        echo "Perulangan Menurun dari 10 ke 1 <br />";
            for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
        }
    ?>
~~~
![image](pict/51.jpg)

# Perulangan while
~~~
<h2>Perulangan While</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
            $i=1;
            while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
            $i++;
        }
    ?>
~~~
![image](pict/61.jpg)

# Perulangan dowhile
~~~
<h2>Perulangan Dowhile</h2>
    <?php
        echo "Perulangan 1 sampai 10 <br />";
            $i=1;
            do {
        echo "Perulangan ke: " . $i . '<br />';
            $i++;
            } while ($i<=10);
    ?>
~~~
![image](pict/71.jpg)

# Pertanyaan dan Tugas
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Tugas 7";
    ?>
<h2>Pertanyaan dan Tugas</h2>
    <form method="post">
            <label>Nama Lengkap: </label>
            <input type="text" name="nama">
            <br>
            <label>Tempat Lahir: </label>
            <input type="text" name="tempat_lahir">
            <br>
            <label>Tanggal Lahir: </label>
            <input type="date" name="tgl_lahir">
            <br>
            <label>Alamat: </label>
            <input type="text" name="alamat">
            <br>
            <label>Pekerjaan:
            <select name='pekerjaan'>
                <option value='Asisten Manajer'>Asisten Manajer</option>
                <option value='Manajer'>Manajer</option>
                <option value='General Manajer'>General Manajer</option>
                <option value='Direktur'>Direktur</option>
            </select>
            </label>
            <br>
            <input type="submit" value="Kirim">
    </form>
    <h2>Output</h2>
    <?php
        echo '<br> Nama Lengkap : ' . $_POST['nama'];
        echo '<br> Tempat Lahir : ' . $_POST['tempat_lahir'];
        echo '<br> Alamat : ' . $_POST['alamat'];
            $tgl_lahir = @$_POST['tgl_lahir'];
            $lahir = new DateTime($tgl_lahir);
            $hari_ini = new DateTime();
            $diff = $hari_ini->diff($lahir);
        echo "<br> Usia : ". $diff->y ." Tahun";
        echo "<br> Pekerjaan : ". $_POST['pekerjaan'];
            $pekerjaan = @$_POST['pekerjaan'];
            if($pekerjaan == "Asisten Manajer"){
                echo '<br> Gaji : Rp. 8.000.000,-';
            }
            elseif($pekerjaan == "Manajer"){
                echo '<br> Gaji : Rp. .10.000.000,-';
            }
            elseif($pekerjaan == "General Manajer"){
                echo '<br> Gaji : Rp. 30.000.000,-';
            }
            elseif($pekerjaan == "Direktur"){
                echo '<br> Gaji : Rp. 100.000.000,-';
            }
    ?>
</body>
</html>
~~~
![image](pict/soal.jpg)
