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
    <h1>🇮🇳 India Calculator Hub</h1>
<p>Smart • Fast • Free Online Calculators</p>
}

header {
    background: #ffffff;
    text-align: center;
    padding: 25px 15px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

header h1 {
    margin: 0;
    font-size: 28px;
}

header p {
    color: #666;
}

.container {
    max-width: 900px;
    margin: auto;
    padding: 20px;
}

.calculator-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 18px;
}



.calc-button:hover {
    transform: translateY(-2px);
}
.calc-button:active {
    transform: scale(0.97);
}
.calc-button {
    border: none;
    background: linear-gradient(135deg, #ffffff, #eef5ff);
    padding: 22px;
    border-radius: 16px;
    font-size: 18px;
    font-weight: 600;
    color: #1e3a8a;
    cursor: pointer;
    box-shadow: 0 4px 12px rgba(0,0,0,0.12);
    transition: all 0.25s ease;
}

.calc-button:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 18px rgba(37,99,235,0.2);
}
 .calc-button:active {
    transform: scale(0.97);
 }   

.calculator.active {
    display: block;
}

input {
    width: 100%;
    padding: 13px;
    margin: 8px 0;
    border: 1px solid #d1d5db;
    border-radius: 9px;
    font-size: 16px;
    outline: none;
    transition: all 0.2s ease;
    box-sizing: border-box;
}

input:focus {
    border-color: #2563eb;
    box-shadow: 0 0 0 3px rgba(37,99,235,0.12);
}

.action {
    width: 100%;
    padding: 14px;
    margin-top: 10px;
    border: none;
    border-radius: 10px;
    background: linear-gradient(135deg, #2563eb, #1d4ed8);
    color: white;
    font-size: 17px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.25s ease;
    box-shadow: 0 4px 10px rgba(37,99,235,0.25);
}

.action:hover {
    transform: translateY(-2px);
    box-shadow: 0 7px 15px rgba(37,99,235,0.3);
}

.action:active {
    transform: scale(0.98);
}

.back {
    background: linear-gradient(135deg, #64748b, #475569);
    box-shadow: 0 4px 10px rgba(71,85,105,0.2);
}

.back:hover {
    transform: translateY(-2px);
    box-shadow: 0 7px 15px rgba(71,85,105,0.25);
}

.result {
    margin-top: 18px;
    padding: 15px;
    background: linear-gradient(135deg, #eef5ff, #e0ecff);
    border-left: 5px solid #2563eb;
    border-radius: 10px;
    font-weight: 600;
    font-size: 17px;
    color: #1e3a8a;
    box-shadow: 0 3px 10px rgba(37,99,235,0.1);
}

footer {
    text-align: center;
    padding: 30px;
    color: #666;
}
</style>
</head>

<body>

<header>
    <h1>🇮🇳 India Calculator Hub</h1>
    <p>Free Online Calculators</p>
</header>

<div class="container">

    <h2>Choose a Calculator</h2>

    <div class="calculator-list">
        <button class="calc-button" onclick="showCalc('age')">
            🎂 Age Calculator
        </button>

        <button class="calc-button" onclick="showCalc('percentage')">
            💯 Percentage Calculator
        </button>

        <button class="calc-button" onclick="showCalc('date')">
            📅 Date Calculator
        </button>

        <button class="calc-button" onclick="showCalc('bmi')">
            ⚖️ BMI Calculator
        </button>

        <button class="calc-button" onclick="showCalc('discount')">
            💰 Discount Calculator
        </button>
    </div>


    <!-- AGE CALCULATOR -->
    <div id="age" class="calculator">
        <h2>🎂 Age Calculator</h2>

        <label>Date of Birth</label>
        <input type="date" id="dob">

        <button class="action" onclick="calculateAge()">
            Calculate Age
        </button>

        <div id="ageResult" class="result"></div>

        <button class="action back" onclick="goBack()">
            ← Back
        </button>
    </div>


    <!-- PERCENTAGE CALCULATOR -->
    <div id="percentage" class="calculator">
        <h2>💯 Percentage Calculator</h2>

        <input type="number" id="obtained" placeholder="Obtained Marks">

        <input type="number" id="total" placeholder="Total Marks">

        <button class="action" onclick="calculatePercentage()">
            Calculate Percentage
        </button>

        <div id="percentageResult" class="result"></div>

        <button class="action back" onclick="goBack()">
            ← Back
        </button>
    </div>


    <!-- DATE CALCULATOR -->
    <div id="date" class="calculator">
        <h2>📅 Date Difference Calculator</h2>

        <label>Start Date</label>
        <input type="date" id="startDate">

        <label>End Date</label>
        <input type="date" id="endDate">

        <button class="action" onclick="calculateDateDifference()">
            Calculate Difference
        </button>

        <div id="dateResult" class="result"></div>

        <button class="action back" onclick="goBack()">
            ← Back
        </button>
    </div>


    <!-- BMI CALCULATOR -->
    <div id="bmi" class="calculator">
        <h2>⚖️ BMI Calculator</h2>

        <input type="number" id="weight" placeholder="Weight (kg)">

        <input type="number" id="height" placeholder="Height (cm)">

        <button class="action" onclick="calculateBMI()">
            Calculate BMI
        </button>

        <div id="bmiResult" class="result"></div>

        <button class="action back" onclick="goBack()">
            ← Back
        </button>
    </div>


    <!-- DISCOUNT CALCULATOR -->
    <div id="discount" class="calculator">
        <h2>💰 Discount Calculator</h2>

        <input type="number" id="price" placeholder="Original Price">

        <input type="number" id="discountPercent" placeholder="Discount %">

        <button class="action" onclick="calculateDiscount()">
            Calculate Discount
        </button>

        <div id="discountResult" class="result"></div>

        <button class="action back" onclick="goBack()">
            ← Back
        </button>
    </div>

</div>

<footer>
    © 2026 India Calculator Hub
</footer>


<script>

function showCalc(id) {
    document.querySelectorAll(".calculator").forEach(function(calc) {
        calc.classList.remove("active");
    });

    document.getElementById(id).classList.add("active");

    window.scrollTo({
        top: document.getElementById(id).offsetTop - 20,
        behavior: "smooth"
    });
}

function goBack() {
    document.querySelectorAll(".calculator").forEach(function(calc) {
        calc.classList.remove("active");
    });

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}


// AGE CALCULATOR
function calculateAge() {

    let dob = new Date(document.getElementById("dob").value);

    if (!document.getElementById("dob").value) {
        document.getElementById("ageResult").innerHTML =
            "Please select your date of birth.";
        return;
    }

    let today = new Date();

    let age = today.getFullYear() - dob.getFullYear();

    let month = today.getMonth() - dob.getMonth();

    if (
        month < 0 ||
        (month === 0 && today.getDate() < dob.getDate())
    ) {
        age--;
    }

    document.getElementById("ageResult").innerHTML =
        "Your age is " + age + " years.";
}


// PERCENTAGE
function calculatePercentage() {

    let obtained = parseFloat(
        document.getElementById("obtained").value
    );

    let total = parseFloat(
        document.getElementById("total").value
    );

    if (!obtained || !total || total <= 0) {
        document.getElementById("percentageResult").innerHTML =
            "Please enter valid marks.";
        return;
    }

    let percentage = (obtained / total) * 100;

    document.getElementById("percentageResult").innerHTML =
        "Percentage: " + percentage.toFixed(2) + "%";
}


// DATE DIFFERENCE
function calculateDateDifference() {

    let start = new Date(
        document.getElementById("startDate").value
    );

    let end = new Date(
        document.getElementById("endDate").value
    );

    if (
        !document.getElementById("startDate").value ||
        !document.getElementById("endDate").value
    ) {
        document.getElementById("dateResult").innerHTML =
            "Please select both dates.";
        return;
    }

    let difference = Math.abs(end - start);

    let days = Math.ceil(
        difference / (1000 * 60 * 60 * 24)
    );

    document.getElementById("dateResult").innerHTML =
        "Difference: " + days + " days";
}


// BMI
function calculateBMI() {

    let weight = parseFloat(
        document.getElementById("weight").value
    );

    let height = parseFloat(
        document.getElementById("height").value
    );

    if (!weight || !height || height <= 0) {
        document.getElementById("bmiResult").innerHTML =
            "Please enter valid weight and height.";
        return;
    }

    let heightMeter = height / 100;

    let bmi = weight / (heightMeter * heightMeter);

    let category = "";

    if (bmi < 18.5) {
        category = "Underweight";
    } else if (bmi < 25) {
        category = "Normal";
    } else if (bmi < 30) {
        category = "Overweight";
    } else {
        category = "Obesity";
    }

    document.getElementById("bmiResult").innerHTML =
        "BMI: " + bmi.toFixed(2) + "<br>Category: " + category;
}


// DISCOUNT
function calculateDiscount() {

    let price = parseFloat(
        document.getElementById("price").value
    );

    let discountPercent = parseFloat(
        document.getElementById("discountPercent").value
    );

    if (
        !price ||
        !discountPercent ||
        price < 0 ||
        discountPercent < 0
    ) {
        document.getElementById("discountResult").innerHTML =
            "Please enter valid values.";
        return;
    }

    let discountAmount =
        price * discountPercent / 100;

    let finalPrice =
        price - discountAmount;

    document.getElementById("discountResult").innerHTML =
        "Discount: ₹" + discountAmount.toFixed(2) +
        "<br>Final Price: ₹" + finalPrice.toFixed(2);
}

</script>
<section style="background:white; padding:20px; margin:20px 0; border-radius:12px; box-shadow:0 3px 10px rgba(0,0,0,0.1);">
    <h2>✨ Why Use India Calculator Hub?</h2>
    <p>Fast, simple and free online calculators for everyday needs.</p>
    <p>🎂 Age &nbsp; 💯 Percentage &nbsp; 📅 Date &nbsp; ⚖️ BMI &nbsp; 💰 Discount</p>
</section>
</body>
</html>
