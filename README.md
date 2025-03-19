<!DOCTYPE html>
<html>
<head>
    <script language="JavaScript1.2">
        var howOften = 3; //number often in seconds to rotate
        var current = 0; //start the counter at 0
        var ns6 = document.getElementById&&!document.all; //detect netscape 6

        // place your images, text, etc in the array elements here
        var items = new Array();

        items[0]= "<img src='Apna Bazar Generic POS.jpg' alt='' border='0' width='850' height='730'>";
        items[1]= "<img src='Apna Bazar Ramadan.jpg' alt='' border='0' width='850' height='730'>";

        function rotater() {
            document.getElementById("placeholderdiv").innerHTML = items[current];
            current = (current == items.length - 1) ? 0 : current + 1;
            setTimeout(rotater, howOften * 1000);
        }
        window.onload = rotater;
    </script>
</head>
<body style="height: 96%;overflow-y: hidden;">
    <div id="parent" style="width: 100%;height: 96%;display: table;text-align: center;">
        <div id="placeholderdiv" style="display: table-cell;vertical-align: middle;"></div>
    </div>
</body>
</html>
