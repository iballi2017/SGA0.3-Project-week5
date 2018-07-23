<!DOCTYPE html>
<html>
<head><title>Calculator</title>
<style type="text/css">
#display{
	position :relative;
	top:2px;
	left:2px;
	text-align:right;
	font-size: 21px;
	height:60px;  /*#### */
	width :285px;  /*#### */
	background-color : #000;
	color:#fff;
	padding: 10px;
}
input-placeholder {
	color:white;
	opacity: 1;
}
.btn{
	position :relative;
	top:2px;
	left:2px;
	color:#fff;
	text-align:center;
	font-size: 30px;
	width :70px;  /*#### */
	height :60px;  /*#### */
	background-color:#00f;
	opacity: 0.5;
}
.display{
	background-color:#ccc;
	margin-left:400px;''  /*#### */
	height: 510px; /*#### */
	width:500px;
	padding-top:30px;
}
.btnEqu{
	position :relative;
	top:2px;
	left:2px;
	height:35px;
	color:#fff;
	text-align:center;
	font-size: 30px;
	width :310px;
	height :60px; /*#### */
	background-color:#00f;
	opacity: 0.5;
}
</style>
<script type="text/javascript">
	function c(val){
		document.getElementById("display").value = val;
	}
	function math(val){
		document.getElementById("display").value+=val;
	}
	function e(){
		try{
			c(eval(document.getElementById("display").value));
		}
		catch(e){
			c('Error')
		}
	}

</script>
</head>
<body>
	<form class="display">
	<div align="center">
		<input type="text" id="display" "placeholder="0" readonly><br>
	<p>
		<input type="button" class="btn" value="9" onclick='math("9")'>
		<input type="button" class="btn" value="8" onclick='math("8")'>
		<input type="button" class="btn" value="7" onclick='math("7")'>
		<input type="button" class="btn" value="+" onclick='math("+")'>
	</p>
	<p>
		<input type="button" class="btn" value="6" onclick='math("6")'>
		<input type="button" class="btn" value="5" onclick='math("5")'>
		<input type="button" class="btn" value="4" onclick='math("4")'>
		<input type="button" class="btn" value="-" onclick='math("-")'>
	</p>
	<p>
		<input type="button" class="btn" value="3" onclick='math("3")'>
		<input type="button" class="btn" value="2" onclick='math("2")'>
		<input type="button" class="btn" value="1" onclick='math("1")'>
		<input type="button" class="btn" value="x" onclick='math("*")'>
	</p>
	<p>
		<input type="button" class="btn" value="0" onclick='math("0")'>
		<input type="button" class="btn" value="." onclick='math(".")'>
		<input type="button" class="btn" value="/" onclick='math("/")'>
		<input type="button" class="btn" value="C" onclick='c("")'>
	</p>
		<input type="button" class="btnEqu" value="=" onclick='e()'>
	</div>
	</form>
</body>
</html>
