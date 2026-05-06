<!DOCTYPE html>
<html lang="lo">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Thong Online Shop</title>

<style>

body{
font-family: Arial;
margin:0;
background:#f4f4f4;
text-align:center;
}

header{
background:#2ecc71;
color:white;
padding:15px;
font-size:22px;
}

.container{
padding:20px;
}

.product{
background:white;
padding:15px;
margin:10px;
border-radius:10px;
}

button{
background:#27ae60;
color:white;
border:none;
padding:10px 15px;
border-radius:5px;
margin-top:10px;
}

input{
padding:8px;
margin:5px;
}

.chat{
position:fixed;
bottom:10px;
right:10px;
background:white;
border:1px solid #ccc;
border-radius:10px;
padding:10px;
width:200px;
}

</style>
</head>

<body>

<header>
ຮ້ານ Thong Online Shop
</header>

<div class="container">

<h2>ສິນຄ້າ</h2>

<div id="products"></div>

<h2>ເພີ່ມສິນຄ້າ</h2>

<input id="name" placeholder="ຊື່ສິນຄ້າ"><br>

<input id="price" placeholder="ລາຄາ"><br>

<input type="file"><br>

<button onclick="addProduct()">ເພີ່ມ</button>

<h2>ຊຳລະເງິນ</h2>

<p>ອັບໂຫຼດສະລິບການໂອນ</p>

<input type="file"><br>

<button>ຢືນຢັນການຊຳລະ</button>

</div>

<div class="chat">

<h4>ແຊດ</h4>

<div id="messages"></div>

<input id="msg" placeholder="ພິມຂໍ້ຄວາມ">

<button onclick="send()">ສົ່ງ</button>

</div>

<script>

function addProduct(){

let name=document.getElementById("name").value

let price=document.getElementById("price").value

let product=`
<div class="product">
<h3>${name}</h3>
<p>ລາຄາ ${price} ກີບ</p>
<button onclick="alert('ກະລຸນາແຊດສັ່ງຊື້')">ສັ່ງຊື້</button>
</div>
`

document.getElementById("products").innerHTML+=product

}

function send(){

let msg=document.getElementById("msg").value

document.getElementById("messages").innerHTML+="<p>"+msg+"</p>"

document.getElementById("msg").value=""

}

</script>

</body>
</html>
