<!--Create event driven program for following:
1. Print a table of numbers from 5 to 15 and their squares and cubes using alert.-->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event-Driven Program</title>
</head>
<body>

<script>
    // Function to calculate square and cube of a number
    function calculateSquareAndCube(number) {
        var square = number * number;
        var cube = number * number * number;
        return { square: square, cube: cube };
    }

    // Function to display the table using alert
    function displayTable() {
        var result = "Number\tSquare\tCube\n";
        for (var i = 5; i <= 15; i++) {
            var calculations = calculateSquareAndCube(i);
            result += i + "\t" + calculations.square + "\t" + calculations.cube + "\n";
        }
        alert(result);
    }

    // Trigger the displayTable function when the page is loaded
    window.onload = displayTable;
</script>

</body>
</html>

