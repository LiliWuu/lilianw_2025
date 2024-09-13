---
layout: post
title: Locations
categories: [Collaboration]
courses: { csse: {week: 3}, csp: {week: 3}, csa: {week: 2} }
menu: nav/pair_programming.html
permalink: location
type: collab
comments: true
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Select your destination</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f9f9f9;
            padding: 40px;
            /* display: flex; */
            justify-content: center;
            align-items: center;
/*             height: 100vh;
            margin: 0; */
        }
        .container {
            background-color: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            display: flex; 
            flex-direction: column;
            gap: 20px;
            align-items: center;
        }
        label {
            font-weight: 600;
            font-size: 1.1em;   
            flex-basis: 100px; 
        }
        select {
            padding: 12px 15px;
            width: 250px;
            border: 1px solid #ccc;
            border-radius: 8px;
            background-color: #fff;
            font-size: 1em;
            color: #333;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: border-color 0.3s, box-shadow 0.3s;
        }
        select:focus {
            border-color: #007bff;
            box-shadow: 0 2px 8px rgba(0, 123, 255, 0.25);
            outline: none;
        }
        select:hover {
            cursor: pointer;
            border-color: #0056b3;
        }
        button {
            padding: 12px 20px;
            font-size: 1em;
            color: #fff;
            background-color: hotpink;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s, box-shadow 0.3s;
            align-self: left;
            margin-top: 20px;
        }
        button:hover {
            background-color: pink;
            box-shadow: 0 2px 8px rgba(0, 123, 255, 0.25);
        }
        .dropdown-group {
            display: flex;
            gap: 15px;
            align-items: center;
            width: 100%;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="dropdown-group">
            <label for="dropdown1">Country</label>
            <select id="dropdown1">
                <option value="">-- Select an Option --</option>
                <option value="tropical">Tropical</option>
                <option value="island">Island</option>
                <option value="city">City</option>
                <option value="desert">Desert</option>
            </select>
        </div>
        <div class="dropdown-group">
            <label for="dropdown2">Cities</label>
            <select id="dropdown2">
                <option value="">-- Select an Option --</option>
            </select>
        </div>
        <button type="button" onclick="handleSubmit()">Select</button>
    </div>
    <script language="javascript">
        const dropdown1 = document.getElementById('dropdown1');
        const dropdown2 = document.getElementById('dropdown2');
        const options = {
            tropical: [
            { value: 'goa, india', text: 'Goa, India' },
            { value: 'cancun, mexico', text: 'Cancun, Mexico' },
            { value: 'rio de janeiro, brazil', text: 'Rio de Janeiro, Brazil' },
            { value: 'bangkok, thailand', text: 'Bangkok, Thailand' },
            { value: 'yucatan peninsula, mexico', text: 'Yucatan Peninsula, Mexico' },
            ],
            island: [
                { value: 'hawaii, USA', text: 'Hawaii, USA' },
                { value: 'bora bora, french polynesia', text: 'Bora Bora, French Polynesia' },
                { value: 'Bahrain', text: 'Bahrain' },
                { value: 'maldives', text: 'Maldives' },
                { value: 'santorini, greece', text: 'Santorini, Greece' },
            ],
            city:[
                { value: 'new york city, USA', text: 'New York City, USA' },
                { value: 'paris, france', text: 'Paris, France' },
                { value: 'london, england', text: 'London, England' },
                { value: 'tokyo, japan', text: 'Tokyo, Japan' },
                { value: 'shanghai, china', text: 'Shanghai, China' },
            ],
             desert: [
                { value: 'cairo, egypt', text: 'Cairo, Egypt' },
                { value: 'las vegas, USA', text: 'Las Vegas, USA' },
                { value: 'phoenix, arizona', text: 'Phoenix, Arizona' },
                { value: 'fez, morocco', text: 'Fez, Morocco' },
                { value: 'jerusalem, israel/palestine', text: 'Jerusalem, Israel/Palestine' },
            ],  
        };
        dropdown1.addEventListener('change', function() {
            const selectedValue = this.value;  
            // Clear previous options in dropdown2
            dropdown2.innerHTML = '<option value="">-- Select an Option --</option>';  
            if (selectedValue) {
                // Populate dropdown2 based on the selected value in dropdown1
                const selectedOptions = options[selectedValue];
                selectedOptions.forEach(option => {
                    const newOption = document.createElement('option');
                    newOption.value = option.value;
                    newOption.textContent = option.text;
                    dropdown2.appendChild(newOption);
                });
            }
        });
        function handleSubmit() {
            const dropdown1Value = document.getElementById('dropdown1').value;
            var dropdown2Value = document.getElementById('dropdown2').value;
            if (dropdown2Value) {
                dropdown2Value = dropdown2Value.split(",")[0].trim();
            }
            if (dropdown1Value && dropdown2Value) {
                // Construct a URL using the selected country and city
                const url = `/lilianw_2025/traveling/${dropdown2Value}/`;
                // Redirect to the constructed URL
                window.location.href = url;
            } else {
                alert('Please select both a country and a city.');
            }
        }
    </script>
    </body>
    </html>


