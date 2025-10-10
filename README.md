# Ex.05 Design a Website for Server Side Processing
## Date: 10-10-2025

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
    <!DOCTYPE html>
    <html>
    <head>
    <title>Power Calculator</title>
    <style>
        body {
            background-color: red;
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 50px;
        }

        h1 {
            color: white;
            font-size: 36px;
            margin-bottom: 30px;
        }

        .form-container {
            display: inline-block;
            text-align: left;
        }

        label {
            color: black;
            font-weight: bold;
            font-size: 14px;
        }

        input[type="text"] {
            width: 120px;
            height: 25px;
            margin-left: 10px;
            border: 1px solid black;
            padding: 3px;
        }

        input[type="submit"] {
            padding: 8px 15px;
            background-color: white;
            border: 1px solid black;
            cursor: pointer;
            font-weight: bold;
            margin: 15px 0;
            display: block;
        }

        input[type="submit"]:hover {
            background-color: lightgray;
        }

        .result {
            color: black;
            font-size: 18px;
            font-weight: bold;
            margin: 20px 0;
        }

        .error {
            color: black;
            font-size: 14px;
            margin: 10px 0;
        }
    </style>
    </head>
    <body>
    <h1>Incandescent Bulb Power Calculator</h1>

    <div class="form-container">
        <form id="powerForm" onsubmit="calculatePower(event)">
            <label for="current">Current (I) in Amps</label>
            <input type="text" id="current" name="current" required><br><br>

            <label for="resistance">Resistance (R) in Ohms</label>
            <input type="text" id="resistance" name="resistance" required><br><br>

            <input type="submit" value="Calculate Power">
        </form>

        <div id="result" class="result" style="display: none;">
            <br>
            Power (P) = <span id="powerValue"></span> Watts<br>
             
        </div>

        <div id="error" class="error" style="display: none;">
             
        </div>
    </div>

    <script>
        function calculatePower(event) {
            event.preventDefault();
            
            const current = parseFloat(document.getElementById('current').value);
            const resistance = parseFloat(document.getElementById('resistance').value);
            
            document.getElementById('error').style.display = 'none';
            document.getElementById('result').style.display = 'none';
            
            if (isNaN(current) || isNaN(resistance)) {
                document.getElementById('error').textContent = 'Please enter valid numbers';
                document.getElementById('error').style.display = 'block';
                return;
            }
            
            const power = Math.pow(current, 2) * resistance;
            
            document.getElementById('powerValue').textContent = power.toFixed(2);
            document.getElementById('result').style.display = 'block';
        }
    </script>
    </body>
    </html>




## SERVER SIDE PROCESSING:
![WhatsApp Image 2025-10-10 at 13 42 44_d89a1d42](https://github.com/user-attachments/assets/48518033-c8be-4989-ae67-13fa3345fe74)



## HOMEPAGE:
<img width="1154" height="455" alt="image" src="https://github.com/user-attachments/assets/48eadede-9be4-48d1-a4fa-db0c3231a7a6" />


## RESULT:
The program for performing server side processing is completed successfully.
