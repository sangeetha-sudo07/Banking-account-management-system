# Banking Account Management System

## Overview
This project is a simple Banking Account Management System developed using HTML, CSS, and JavaScript.

## Features
- Deposit Money
- Withdraw Money
- Check Balance

## Technologies Used
- HTML
- CSS
- JavaScript

## Author
Sangeetha
<!DOCTYPE html>
<html>
<head>
    <title>Banking Account Management System</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Banking Account Management System</h1>

    <input type="number" id="amount" placeholder="Enter Amount">

    <button onclick="deposit()">Deposit</button>
    <button onclick="withdraw()">Withdraw</button>

    <h2 id="balance">Balance: ₹0</h2>

    <script src="script.js"></script>
</body>
</html>
body{
    font-family: Arial, sans-serif;
    background:#f3f4ff;
    text-align:center;
    margin:0;
}

.container{
    padding:40px;
}

h1{
    color:#0a1f70;
}

.card{
    background:white;
    width:80%;
    margin:auto;
    padding:30px;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
}

input{
    width:80%;
    padding:12px;
    margin:15px;
}

.buttons{
    display:flex;
    justify-content:center;
    gap:20px;
}

.deposit{
    background:green;
    color:white;
    padding:12px 25px;
    border:none;
}

.withdraw{
    background:red;
    color:white;
    padding:12px 25px;
    border:none;
}

.balance-box{
    margin-top:20px;
    background:#eef2ff;
    padding:20px;
    border-radius:10px;
}


let balance = 0;

function deposit() {
    let amount = Number(document.getElementById("amount").value);
    balance += amount;
    document.getElementById("balance").innerHTML =
    "Balance: ₹" + balance;
}

function withdraw() {
    let amount = Number(document.getElementById("amount").value);

    if(amount <= balance){
        balance -= amount;
        document.getElementById("balance").innerHTML =
        "Balance: ₹" + balance;
    }
    else{
        alert("Insufficient Balance");
    }
}

https://sangeetha-sudo07.github.io/Banking-account-management-system/
