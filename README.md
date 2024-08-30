mkdir aventador-svj-countdown
cd aventador-svj-countdown


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Countdown for Murtaza</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: url('https://example.com/aventador-svj-background.jpg') no-repeat center center fixed; 
            background-size: cover;
            color: #fff;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background: rgba(0, 0, 0, 0.6); /* Semi-transparent background for better text visibility */
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
            animation: fadeIn 2s ease-in-out;
        }
        .countdown {
            font-size: 3em;
            margin: 20px 0;
            color: #FFDD44; /* Bright color for the countdown */
            animation: bounce 2s infinite;
        }
        .message {
            font-size: 1.5em;
            margin: 20px 0;
            animation: fadeInUp 1.5s ease-in-out;
        }
        .button {
            display: inline-block;
            padding: 10px 20px;
            font-size: 1em;
            color: #fff;
            background-color: #FF5733; /* Cool color for the button */
            border: none;
            border-radius: 5px;
            text-decoration: none;
            transition: background-color 0.3s, transform 0.3s;
            animation: pulse 2s infinite;
        }
        .button:hover {
            background-color: #C70039; /* Darker color on hover */
            transform: scale(1.1);
        }

        /* Animation Keyframes */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-30px);
            }
            60% {
                transform: translateY(-15px);
            }
        }

        @keyframes pulse {
            0% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
            100% {
                transform: scale(1);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Happy Birthday, Murtaza!</h1>
        <div class="countdown" id="countdown"></div>
        <div class="message">
            <p>Hey Mangoman! I can't wait to celebrate with you. Here's a countdown to your special day:</p>
        </div>
      
    </div>
    <script>
        function updateCountdown() {
            const now = new Date();
            const birthday = new Date('2024-11-03T00:00:00'); // Murtaza's birthday
            const diff = birthday - now;
            if (diff < 0) {
                document.getElementById('countdown').innerHTML = "It's your birthday, Mangoman!";
                return;
            }
            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);
            document.getElementById('countdown').innerHTML =
                `${days}d ${hours}h ${minutes}m ${seconds}s`;
        }
        setInterval(updateCountdown, 1000);
        updateCountdown(); // Call once to set initial countdown
    </script>
</body>
</html>

