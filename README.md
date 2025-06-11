# Temperature-Converter
<!DOCTYPE html>
<html>
<head>
  <title>Temperature Converter</title>
</head>
<body>
  <h2>Temperature Converter</h2>
  <input type="number" id="temp" placeholder="Enter temperature">
  <select id="type">
    <option value="CtoF">Celsius to Fahrenheit</option>
    <option value="FtoC">Fahrenheit to Celsius</option>
  </select>
  <button onclick="convertTemp()">Convert</button>
  <p id="output"></p>

  <script>
    function convertTemp() {
      let temp = parseFloat(document.getElementById('temp').value);
      let type = document.getElementById('type').value;
      let converted;

      if (type === "CtoF") {
        converted = (temp * 9/5) + 32;
        document.getElementById('output').innerText = `${temp}°C = ${converted.toFixed(2)}°F`;
      } else {
        converted = (temp - 32) * 5/9;
        document.getElementById('output').innerText = `${temp}°F = ${converted.toFixed(2)}°C`;
      }
    }
  </script>
</body>
</html>
