<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I Love You Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff;
        }
        form {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        input[type="text"] {
            padding: 10px;
            margin: 10px 0;
            width: 100%;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="submit"] {
            background-color: #ff69b4;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #ff1493;
        }
        #message {
            margin-top: 20px;
            font-size: 1.5em;
            color: #ff69b4;
        }
    </style>
</head>
<body>

    <form id="loveForm" onsubmit="return displayMessage(event)">
        <label for="name">Enter your name:</label>
        <input type="text" id="name" name="name" required>
        <input type="submit" value="Submit">
    </form>

    <div id="message"></div>

    <script>
        function displayMessage(event) {
            event.preventDefault(); // Prevent the form from submitting
            const name = document.getElementById('name').value;
            const messageDiv = document.getElementById('message');
            messageDiv.textContent = `I love you, ${name}!`;
        }
    </script>

</body>
</html>

