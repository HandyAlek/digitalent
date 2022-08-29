<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>TUGAS 5</title>

</head>
<body>
    <?php
    function tambah ($x, $y){
        $a = $x + $y;
        return $a;
    }
    function kurang ($x, $y){
        $a = $x - $y;
        return $a;
    }
    function kali ($x, $y){
        $a = $x * $y;
        return $a;
    }
    function bagi ($x, $y){
        $a = ($y !=0) ? $x/$y : 0;
        return $a;
    }
    ?>

    <div class="kalkulator">
        <h2 class="judul">KALKULATOR SEDERHANA</h2>

        <form method="POST" action="a.php">
            <label>Bilangan 1 : </label><input type="text" name="bil1" class="input1" placeholder="Input Angka Ke-1"><br>
            <br>
            <label>Bilangan 2 : </label><input type="text" name="bil2" class="input1" placeholder="Input Angka Ke-2"><br>
            <br>
            <input type="submit" name="hitung" value="Hitung" class="button">
        </form>

        <?php
        echo "<br>";
            if(isset($_POST['hitung'])){
                $bil1 = $_POST['bil1'];
                $bil2 = $_POST['bil2'];

                echo "Hasil Penjumlahan adalah = " .tambah($bil1,$bil2). "<br>";
                echo "Hasil Pengurangan adalah = " .kurang($bil1,$bil2). "<br>";
                echo "Hasil Perkalian adalah = " .kali($bil1,$bil2). "<br>";
                echo "Hasil Pembagian adalah = " .bagi($bil1,$bil2). "<br>";
            }
        ?>
    </div>
</body>
</html>
