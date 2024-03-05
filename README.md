﻿# web-calculator
<html>
<head>
  <title>Calculator</title>
 <link href="C:\Users\ruchi\OneDrive\Desktop\js r/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body {
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .c {
	height:450px;
      width: 320px;
      background-color: #e8e8ff;
      border-radius: 5px;
	  padding:20px;
	  
    }
	.b
	{
	height:50px;
	width:50px;
	margin:10px;
	}
	.b:hover{
	background:rgba(0, 0, 0, 0.2);
	}
  </style>
</head>
<body>

<div class="c">
  <input type="text" id="i1" class="form-control mb-3" readonly>

  <div class="btn-group">
    <button class=" b" onclick="c()">C</button>
    <button class="b" onclick="r('%')">%</button>
	    <button class=" b" onclick="d()">DEL</button>
    <button class="b" onclick="r('/')">/</button>
  </div>

  <div class="btn-group">
    <button class="b" onclick="r('7')">7</button>
    <button class=" b" onclick="r('8')">8</button>
    <button class=" b" onclick="r('9')">9</button>
    <button class=" b" onclick="r('*')">*</button>
  </div>

  <div class="btn-group">
    <button class="b" onclick="r('4')">4</button>
    <button class=" b" onclick="r('5')">5</button>
    <button class=" b" onclick="r('6')">6</button>
    <button class=" b" onclick="r('-')">-</button>
  </div>

  <div class="btn-group">
    <button class="b" onclick="r('1')">1</button>
    <button class="b" onclick="r('2')">2</button>
    <button class=" b" onclick="r('3')">3</button>
	    <button class=" b" onclick="r('+')">+</button>

  </div>

  <div class="btn-group">
    <button class=" b" onclick="r('0')">0</button>
    <button class=" b" onclick="r('.')">.</button>
	    <button class=" b" onclick="cr()">=</button>

  </div>
</div>



<script>
  function r(value) {
    document.getElementById('i1').value += value;
  }

  function c() {
    document.getElementById('i1').value = '';
  }

  function d() {
    var d = document.getElementById('i1').value;
    document.getElementById('i1').value = d.slice(0, -1);
  }

  function cr() {
   var result;
    try {
      result = eval(document.getElementById('i1').value);
    } catch (error) {
      result = 'Error';
    }
    document.getElementById('i1').value = result;
  }
</script>

</body>
</html>
