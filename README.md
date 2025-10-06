# Ex No:5
# Date:04/10/2025
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lamp Filament Power Calculator</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      /* 🌈 Vibrant gradient background */
      background: linear-gradient(135deg, #ff9a9e, #fad0c4, #a1c4fd);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      transition: background 0.5s ease;
    }

    .container {
      background: rgba(255, 255, 255, 0.95); /* slightly transparent */
      padding: 35px;
      border-radius: 25px;
      box-shadow: 0 15px 30px rgba(0,0,0,0.2);
      width: 360px;
      text-align: center;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      backdrop-filter: blur(10px);
    }

    .container:hover {
      transform: scale(1.03);
      box-shadow: 0 20px 40px rgba(0,0,0,0.25);
    }

    h1 {
      color: #ff4b5c;
      font-size: 24px;
      margin-bottom: 10px;
      text-shadow: 1px 1px 5px rgba(0,0,0,0.2);
    }

    p {
      font-weight: 500;
      color: #555;
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-top: 15px;
      font-weight: 600;
      color: #333;
    }

    input {
      width: 85%;
      padding: 10px;
      margin-top: 5px;
      border: 2px solid #ff6b81;
      border-radius: 12px;
      font-size: 16px;
      transition: all 0.3s;
    }

    input:focus {
      border-color: #ff4757;
      box-shadow: 0 0 12px rgba(255,71,87,0.4);
      outline: none;
    }

    button {
      margin-top: 25px;
      background: linear-gradient(90deg, #ff6b81, #ff4757);
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 12px;
      cursor: pointer;
      font-size: 16px;
      font-weight: bold;
      box-shadow: 0 5px 15px rgba(255,71,87,0.4);
      transition: 0.4s;
    }

    button:hover {
      background: linear-gradient(90deg, #ff4757, #ff6b81);
      box-shadow: 0 8px 20px rgba(255,71,87,0.6);
    }

    .result {
      margin-top: 25px;
      font-size: 22px;
      font-weight: bold;
      color: #ff4b5c;
      text-shadow: 0 0 15px rgba(255,75,92,0.6);
      transition: 0.3s;
    }

  </style>
</head>
<body>

  <div class="container">
    <h1>💡 Lamp Filament Power Calculator</h1>
    <p>Formula: <strong>P = I² × R</strong></p>

    <label for="intensity">Enter Intensity (I in Amperes):</label>
    <input type="number" id="intensity" step="any" placeholder="e.g., 0.5">

    <label for="resistance">Enter Resistance (R in Ohms):</label>
    <input type="number" id="resistance" step="any" placeholder="e.g., 10">

    <button onclick="calculatePower()">Calculate Power</button>

    <div class="result" id="result"></div>
  </div>

  <script>
    function calculatePower() {
      const I = parseFloat(document.getElementById('intensity').value);
      const R = parseFloat(document.getElementById('resistance').value);
      const resultDiv = document.getElementById('result');

      if (isNaN(I) || isNaN(R)) {
        resultDiv.textContent = "⚠️ Please enter both Intensity and Resistance.";
        resultDiv.style.color = "red";
        resultDiv.style.textShadow = "0";
        return;
      }

      const P = (I * I * R).toFixed(2);
      resultDiv.style.color = "#ff4b5c";
      resultDiv.style.textShadow = "0 0 15px rgba(255,75,92,0.6)";
      resultDiv.textContent = `Power (P) = ${P} W`;
    }
  </script>

</body>
</html>
```

# SERVER SIDE PROCESSING:
![WhatsApp Image 2025-10-01 at 21 33 37_a011fce1](https://github.com/user-attachments/assets/20f02e64-e078-4ff0-82c5-27e6c34991f4)

# HOMEPAGE:
<img width="1920" height="1080" alt="Screenshot 2025-10-06 200654" src="https://github.com/user-attachments/assets/f6d81709-2edb-462c-aa33-cd653359696d" />

# RESULT:
The program for performing server side processing is completed successfully.
