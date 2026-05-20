# Thank-you-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Anniversary</title>
    <style>
        /* Full-screen setup */
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        /* Centered message container */
        .card {
            text-align: center;
            padding: 40px;
            border-radius: 20px;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
            border: 1px solid rgba(255, 255, 255, 0.1);
            max-width: 80%;
            animation: fadeIn 1.5s ease-in-out;
        }

        h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: #4e9af1;
        }

        p {
            font-size: 1.5rem;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .signature {
            font-style: italic;
            color: #00b4d8;
            font-weight: bold;
        }

        /* Top-right exit button */
        #exitBtn {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 12px 24px;
            background-color: #e63946;
            color: white;
            border: none;
            border-radius: 30px;
            font-size: 1rem;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(230, 57, 70, 0.4);
            transition: all 0.3s ease;
            opacity: 0;
            pointer-events: none; /* Invisible and unclickable initially */
        }

        #exitBtn.show {
            opacity: 1;
            pointer-events: auto; /* Clickable after 5 seconds */
        }

        #exitBtn:hover {
            background-color: #d62828;
            transform: scale(1.05);
        }

        /* Simple animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="card">
        <h1>Happy Anniversary!</h1>
        <p>Thank you, <span id="userName" style="color: #ffb703; font-weight: bold;"></span>, for being with us for this anniversary.</p>
        <p class="signature">— With love, Lila School</p>
    </div>

    <!-- Hidden exit button -->
    <button id="exitBtn" onclick="exitPage()">Exit</button>

    <script>
        // Ask for the user's name immediately on load
        window.onload = function() {
            let name = prompt("Please enter your name:");
            
            // Default to "Guest" if they leave it empty or cancel
            if (!name || name.trim() === "") {
                name = "Guest";
            }
            
            // Insert name into the page
            document.getElementById("userName").innerText = name;

            // Wait 5 seconds (5000 milliseconds) then show the exit button
            setTimeout(function() {
                document.getElementById("exitBtn").classList.add("show");
            }, 5000);
        };

        // Function for the exit button action
        function exitPage() {
            // Replaces the current page with a blank space or attempts to close
            window.location.href = "about:blank"; 
        }
    </script>
</body>
</html>

