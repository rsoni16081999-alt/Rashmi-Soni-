<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>India Calculator Hub</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f5f7fb;
      color: #222;
    }

    header {
      background: #1f4e79;
      color: white;
      text-align: center;
      padding: 25px 15px;
    }

    header h1 {
      margin: 0;
      font-size: 30px;
    }

    header p {
      margin: 8px 0 0;
    }

    .container {
      max-width: 900px;
      margin: auto;
      padding: 20px;
    }

    .calculator-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 15px;
    }

    .calculator-button {
      border: none;
      background: white;
      padding: 20px 10px;
      border-radius: 12px;
      cursor: pointer;
      font-size: 16px;
      font-weight: bold;
      box-shadow: 0 3px 10px rgba(0,0,0,0.08);
    }

    .calculator-button:hover {
      transform: translateY(-2px);
    }

    .calculator {
      display: none;
      background: white;
      margin-top: 25px;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.08);
    }

    .calculator.active {
      display: block;
    }

    input {
      width: 100%;
      padding: 12px;
      margin: 8px 0 15px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
    }

    .calculate-btn {
      background: #1f4e79;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
    }

    .result {
      margin-top: 15px;
      font-weight: bold;
      line-height: 1.8;
    }

    footer {
      text-align: center;
      padding: 25px;
      margin-top: 30px;
      background: #222;
      color: white;
    }
  </style>
</head>

<body>

<header>
  <h1>India Calculator Hub</h1>
  <p>Simple, Fast & Free Online Calculators</p>
</header>

<div class="container">

  <h2>Choose a Calculator</h2>

  <div class="calculator-grid">

    <button class="calculator-button" onclick="openCalculator('age')">
      🎂 Age Calculator
    </button>

    <button class="calculator-button" onclick="openCalculator('percentage')">
      💯 Percentage
    </button>

    <button class="calculator-button" onclick="openCalculator('bmi')">
      ⚖️ BMI Calculator
    </button>

    <button class="calculator-button" onclick="openCalculator('date')">
      📅 Date Difference
    </button>

    <button class="calculator-button" onclick="openCalculator('discount')">
      💰 Discount Calculator
    </button>

    <button class="calculator-button" onclick="openCalculator('emi')">
      🏦 EMI Calculator
    </button>

    <button class="calculator-button" onclick="openCalculator('gst')">
      🧾 GST Calculator
    </button>

    <button class="calculator-button" onclick="openCalculator('simpleInterest')">
      💵 Simple Interest
    </button>

    <button class="calculator-button" onclick="openCalculator('compoundInterest')">
      📈 Compound Interest
    </button>

    <button class="calculator-button" onclick="openCalculator('loan')">
      🏠 Loan Calculator
    </button>

  </div>

  <!-- Calculators will be added here -->

  <div id="calculatorArea"></div>

</div>

<footer>
  © 2026 India Calculator Hub
</footer>

<script>

function openCalculator(type) {

  const area = document.getElementById("calculatorArea");

  area.innerHTML = "";

  if (type === "age") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>🎂 Age Calculator</h2>
        <p>Age calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "percentage") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>💯 Percentage Calculator</h2>
        <p>Percentage calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "bmi") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>⚖️ BMI Calculator</h2>
        <p>BMI calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "date") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>📅 Date Difference</h2>
        <p>Date calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "discount") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>💰 Discount Calculator</h2>
        <p>Discount calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "emi") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>🏦 EMI Calculator</h2>
        <p>EMI calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "gst") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>🧾 GST Calculator</h2>
        <p>GST calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "simpleInterest") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>💵 Simple Interest</h2>
        <p>Simple Interest calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "compoundInterest") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>📈 Compound Interest</h2>
        <p>Compound Interest calculator will be added next.</p>
      </div>
    `;
  }

  if (type === "loan") {
    area.innerHTML = `
      <div class="calculator active">
        <h2>🏠 Loan Calculator</h2>
        <p>Loan calculator will be added next.</p>
      </div>
    `;
  }

  area.scrollIntoView({
    behavior: "smooth"
  });
}

</script>

</body>
</html>
