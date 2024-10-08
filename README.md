<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wedding Greeting Card</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f7f0f5;
        }
        .card {
            background-color: white;
            width: 400px;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        h1 {
            color: #c49bbb;
        }
        .message {
            font-size: 1.2em;
            color: #555;
            margin: 20px 0;
        }
        .image-container img {
            width: 100%;
            border-radius: 10px;
        }
        .footer {
            font-size: 1em;
            color: #7d5a91;
            margin-top: 20px;
        }
        .congrats {
            font-weight: bold;
            font-size: 1.5em;
            color: #ff6b6b;
            margin-top: 10px;
        }
        .blessings {
            margin-top: 30px;
        }
        .blessings input, .blessings textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .blessings textarea {
            height: 80px;
            resize: none;
        }
        .blessings button {
            background-color: #c49bbb;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .blessings button:hover {
            background-color: #a26fa6;
        }
        .output {
            margin-top: 20px;
            font-size: 1.1em;
            color: #555;
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>Congratulations on Your Wedding!</h1>
        
        <div class="image-container">
            <img src="https://example.com/wedding-photo.jpg" alt="Wedding Image">
        </div>

        <p class="message">
            Wishing you both a lifetime of love, laughter, and happiness. May this journey be full of wonderful memories and endless joy!
        </p>

        <div class="footer">
            <p>Best wishes from all of us!</p>
            <p class="congrats">🎉 Congratulations! 🎉</p>
        </div>

        <!-- Blessing Form -->
        <div class="blessings">
            <h2>Leave Your Blessings</h2>
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="text" id="surname" placeholder="Your Surname" required>
            <textarea id="blessing" placeholder="Write your blessings here..." required></textarea>
            <button onclick="displayBlessing()">Submit Blessing</button>

            <!-- Display User's Blessing -->
            <div class="output" id="output"></div>
        </div>
    </div>

    <script>
        function displayBlessing() {
            var name = document.getElementById("name").value;
            var surname = document.getElementById("surname").value;
            var blessing = document.getElementById("blessing").value;

            if (name && surname && blessing) {
                document.getElementById("output").innerHTML = 
                    "<strong>" + name + " " + surname + ":</strong> " + blessing;
            } else {
                alert("Please fill in all fields before submitting.");
            }
        }
    </script>

</body>
</html>
