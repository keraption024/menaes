# <!DOCTYPE HTML>
<html>
<body>
    <form method="post" action="">
        Starting Number: <input type="number" name="start"><br>
        Ending Number: <input type="number" name="end"><br>
        <input type="submit" name="display" value="Submit">
    </form>

    <?php
    if (isset($_POST['display'])) {
        $start = $_POST['start'];
        $end = $_POST['end'];

        $odd = ($start % 2 != 0) ? $start : $start + 1;
        $even = ($start % 2 == 0) ? $start : $start + 1;

        echo "Odd Numbers: ";
        for ($i = $odd; $i <= $end; $i += 2) {
            echo $i . " ";
        }

        echo "<br>Even Numbers: ";
        for ($i = $even; $i <= $end; $i += 2) {
            echo $i . " ";
        }
    }
    ?>
</body>
</html>
