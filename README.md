<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="utf-8">
<title>wielowymiar </title>
<link rel="stylesheet" type="text/css" href="stylW1.css">
<script>

 var tab = [
    ["4", "2", "1", "3"],
    ["1", "3", "4", "2"],
    ["2", "1", "3", "4"],
	["3", "4", "2", "1"]
];
/*
document.write("<table border='1px'>");
for(var i=0; i<=3; i++)
{
document.write("<tr>")
for(var j=0; j<=3; j++){
document.write("<td>"+tab[i][j]+"</td>")
}
document.write("</tr>")
} */


function spr(){
var td00=document.getElementById('t00').value;
var td01=document.getElementById('t01').value;
var td02=document.getElementById('t02').value;
var td03=document.getElementById('t03').value;
if (td00==tab[0][0]) document.getElementById('t00').style.color = "green";
else document.getElementById('t00').style.color = "red";

if (td01==tab[0][1]) document.getElementById('t01').style.color = "green";
else document.getElementById('t01').style.color = "red";

if (td02==tab[0][2]) document.getElementById('t02').style.color = "green";
else document.getElementById('t02').style.color = "red";

if (td03==tab[0][3]) document.getElementById('t03').style.color = "green";
else document.getElementById('t03').style.color = "red";
}

</script>
<style>
table,td{
border: 1px solid black;
border-collapse: collapse;
text-align: center;
height: 220px;
width: 220px;
}
td{
width: 50px;
height: 30px;}
.ob{
border-right: 3px solid black;}
.ob2{
border-bottom: 3px solid black;}
input{
	height: 28px;
	width: 28px;
	border: none;
	font-size: 15px;
	font-weight: bold;
	text-align: center;	}
#sp{
width: 200px;
margin-left: 10px;}
</style>
</head>
<body>
<br>
<form>
<table>
<tr> <td><input type="text" id="t00"> </td> <td class='ob'><input type="text" id="t01"> </td> <td><input type="text" id="t02"> </td> <td> <input type="text" id="t03"></td> </tr>
<tr class='ob2'> <td> <input type="text" id="t10"></td> <td class='ob'> 3 </td> <td> 4</td> <td> 2</td> </tr>
<tr> <td> 2</td> <td class='ob'>1 </td> <td> 3</td> <td><input type="text" id="t23"> </td> </tr>
<tr> <td><input type="text" id="t30"> </td> <td class='ob'><input type="text" id="t31"> </td> <td><input type="text" id="t32"> </td> <td><input type="text" id="t33"> </td> </tr>
</table>
<input type="button" onclick="spr()" value="sprawdz" id="sp">
</form>
</body>
</html>
