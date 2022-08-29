<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>TUGAS 5</title>
    <style>
        body{
            background-color: aliceblue;
        }
        .kalkulator {
            font-size: 20px;
            font-family: 'Courier New', Courier, monospace;
            background-color: aqua;
            border-radius: 24px;
            width: 500px;
            padding: 30px;
            margin: 30px auto;
        }
        .button{
            background-color:black;
            border-radius: 24px;
            color: white;
            padding: 5px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
        }
        .input1{
            border: none;
            border-radius: 24px;
            width: 250px;
            font-size: 20px;
            padding: 5px;
        }
        input::-webkit-input-placeholder{
            color: gray;
            opacity: 0.5;
            font-size: 16px;
            padding: 10px;
        }
    </style>

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
