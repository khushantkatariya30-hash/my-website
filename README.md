<!DOCTYPE html>
<html>
<head>
  <title>Roll Number Verification</title>
  <style>
    body {
      font-family: Arial;
      background: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .box {
      background: white;
      padding: 20px;
      border-radius: 10px;
      width: 300px;
      text-align: center;
    }
    input {
      width: 90%;
      padding: 8px;
      margin: 8px 0;
    }
    button {
      padding: 8px 20px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<div class="box">
  <h3>Enter Roll Number</h3>

  <input type="text" id="roll" placeholder="Roll Number">

  <p>Captcha: <b>1234</b></p>
  <input type="text" id="captcha" placeholder="Enter Captcha">

  <button onclick="check()">Submit</button>
  <p id="msg" style="color:red;"></p>
</div>

<script>
function check() {
  var roll = document.getElementById("roll").value;
  var cap = document.getElementById("captcha").value;

  if (roll === "2400709023" && cap === "1234") {
    window.location.href = "paper.html";
  } else {
    document.getElementById("msg").innerText = "Wrong Roll Number or Captcha";
  }
}
</script>

</body>
</html>
