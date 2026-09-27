# Coll-top-up
<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>FF TopUp</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
  font-family:Arial,sans-serif;
}

body{
  background:#080b12;
  color:white;
}

header{
  background:#111827;
  padding:18px;
  text-align:center;
  border-bottom:1px solid #293244;
}

.logo{
  color:#ffd21c;
  font-size:28px;
  font-weight:bold;
}

.hero{
  text-align:center;
  padding:45px 20px;
  background:linear-gradient(135deg,#171d32,#090b12);
}

.hero h1{
  font-size:36px;
  margin-bottom:12px;
}

.hero p{
  color:#b9c0ce;
}

.container{
  max-width:900px;
  margin:auto;
  padding:25px 15px;
}

.card{
  background:#121722;
  padding:22px;
  border-radius:18px;
  margin-bottom:20px;
  border:1px solid #293244;
}

.card h2{
  margin-bottom:18px;
}

.packages{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:12px;
}

.package{
  background:#181e2b;
  border:1px solid #30394d;
  padding:18px;
  border-radius:12px;
  text-align:center;
  cursor:pointer;
}

.package:hover,
.package.selected{
  border-color:#ffd21c;
  background:#202638;
}

.diamond{
  color:#ffd21c;
  font-size:23px;
  font-weight:bold;
}

.price{
  margin-top:8px;
  color:#ddd;
}

label{
  display:block;
  margin-top:14px;
  margin-bottom:6px;
}

input,select{
  width:100%;
  padding:14px;
  border-radius:10px;
  border:1px solid #30394d;
  background:#090d15;
  color:white;
  outline:none;
}

button{
  width:100%;
  margin-top:20px;
  padding:15px;
  border:none;
  border-radius:10px;
  background:#ffd21c;
  color:#111;
  font-size:17px;
  font-weight:bold;
  cursor:pointer;
}

button:hover{
  background:#ffdf55;
}

#result{
  display:none;
  margin-top:18px;
  padding:15px;
  background:#10301b;
  border-radius:10px;
  color:#9ff0b0;
  line-height:1.8;
}

.note{
  color:#8d96a8;
  font-size:12px;
  margin-top:15px;
  line-height:1.5;
}

footer{
  text-align:center;
  padding:25px;
  color:#737b8b;
}

@media(max-width:650px){
  .packages{
    grid-template-columns:repeat(2,1fr);
  }

  .hero h1{
    font-size:29px;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">🔥 FF TOPUP</div>
</header>

<section class="hero">
  <h1>Free Fire Diamond Top Up</h1>
  <p>দ্রুত ও সহজে আপনার Player UID দিয়ে অর্ডার করুন</p>
</section>

<div class="container">

<div class="card">

<h2>💎 Diamond Package</h2>

<div class="packages">

<div class="package" onclick="selectPackage(this,'25','25')">
<div class="diamond">25 💎</div>
<div class="price">৳25</div>
</div>

<div class="package" onclick="selectPackage(this,'50','45')">
<div class="diamond">50 💎</div>
<div class="price">৳45</div>
</div>

<div class="package" onclick="selectPackage(this,'115','90')">
<div class="diamond">115 💎</div>
<div class="price">৳90</div>
</div>

<div class="package" onclick="selectPackage(this,'240','180')">
<div class="diamond">240 💎</div>
<div class="price">৳180</div>
</div>

<div class="package" onclick="selectPackage(this,'610','430')">
<div class="diamond">610 💎</div>
<div class="price">৳430</div>
</div>

<div class="package" onclick="selectPackage(this,'1240','850')">
<div class="diamond">1240 💎</div>
<div class="price">৳850</div>
</div>

</div>
</div>


<div class="card">

<h2>🧾 Order Information</h2>

<label>Free Fire Player UID</label>

<input
type="number"
id="uid"
placeholder="আপনার Player UID লিখুন"
>


<label>Payment Method</label>

<select id="payment">

<option value="bKash">bKash</option>

<option value="Nagad">Nagad</option>

<option value="Manual">Manual Payment</option>

</select>
