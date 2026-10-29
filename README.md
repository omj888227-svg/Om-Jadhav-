# Om-Jadhav-
My calculator 
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <style>
        body {
            background-color: #0f172a;
            color: #38bdf8;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .clock-container {
            text-align: center;
            background: #1e293b;
            padding: 30px 60px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5), 0 0 20px rgba(56, 189, 248, 0.2);
        }
        #time {
            font-size: 4rem;
            font-weight: bold;
            letter-spacing: 2px;
            margin: 0;
        }
        #date {
            color: #94a3b8;
            font-size: 1.2rem;
            margin-top: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
    </style>
</head>
<body>

    <div class="clock-container">
        <div id="time">00:00:00 PM</div>
        <div id="date">Loading Date...</div>
    </div>

    <script>
        function updateClock() {
            const now = new Date();
            
            // Format Time
            let timeString = now.toLocaleTimeString();
            document.getElementById('time').textContent = timeString;
            
            // Format Date
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            let dateString = now.toLocaleDateString(undefined, options);
            document.getElementById('date').textContent = dateString;
        }

        setInterval(updateClock, 1000);
        updateClock(); // Run immediately
    </script>
</body>
</html>