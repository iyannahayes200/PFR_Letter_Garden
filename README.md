# PFR_Letter_Garden
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Sonja 🌸</title>
    <style>
        /* Base Styling & Forest Green Theme */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #1b4332; /* Forest Green */
            color: #d8f3dc;
            text-align: center;
            padding: 20px;
            margin: 0;
        }
        
        h1, h2, p {
            margin-bottom: 20px;
        }

        /* Password Screen Container */
        #password-screen {
            max-width: 500px;
            margin: 100px auto;
            background: #2d6a4f;
            padding: 40px 20px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
            border: 2px solid #ffb3c1;
        }

        .hint {
            font-size: 18px;
            color: #ffb3c1; /* Pink hint text */
            font-weight: bold;
            line-height: 1.5;
        }

        input[type="password"] {
            padding: 12px;
            width: 80%;
            max-width: 250px;
            border-radius: 8px;
            border: 2px solid #ffb3c1;
            background-color: #1b4332;
            color: #fff;
            font-size: 18px;
            text-align: center;
            margin-bottom: 20px;
            letter-spacing: 2px;
        }

        .btn-unlock {
            background-color: #ffb3c1;
            color: #1b4332;
            border: none;
            padding: 12px 30px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            transition: 0.2s;
        }

        .btn-unlock:hover {
            background-color: #ff758f;
            color: white;
        }

        #error-msg {
            color: #ff4d6d;
            font-weight: bold;
            margin-top: 10px;
            display: none;
        }

        /* Main Content Screen (Hidden Initially) */
        #main-content {
            display: none;
            max-width: 700px;
            margin: 0 auto;
            animation: fadeIn 0.8s ease-in-out;
        }

        .title-banner {
            color: #ffb3c1;
            font-size: 32px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }

        /* Grid arrangement for buttons */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
            margin: 30px auto;
        }

        /* Mood Button Styles */
        .mood-btn {
            background-color: #2d6a4f;
            border: 2px solid #ffb3c1;
            padding: 15px;
            border-radius: 12px;
            font-size: 15px;
            font-weight: bold;
            color: #ffb3c1;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0,0,0,0.2);
        }

        .mood-btn:hover {
            background-color: #ffb3c1;
            color: #1b4332;
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(255, 179, 193, 0.4);
        }

        /* The Pink Paper Note Pop-up Box */
        #letter-box {
            background: #ffe5ec; /* Pink paper color */
            color: #4c1c24; /* Dark pink/burgundy text */
            padding: 30px;
            border-radius: 15px;
            max-width: 550px;
            margin: 30px auto;
            display: none;
            box-shadow: 0 10px 20px rgba(0,0,0,0.4);
            border-left: 8px solid #ff758f;
            text-align: left;
            position: relative;
            line-height: 1.6;
            font-size: 17px;
            white-space: pre-line; /* Preserves line breaks from your text */
            animation: slideDown 0.4s ease-out;
        }

        #letter-title {
            color: #ff4d6d;
            margin-top: 0;
            border-bottom: 2px dashed #ffb3c1;
            padding-bottom: 10px;
            font-size: 22px;
        }

        /* Decorative Lilies Styling */
        .lily-deco {
            font-size: 24px;
            margin: 10px;
            display: inline-block;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes slideDown {
            from { transform: translateY(-20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
    </style>
</head>
<body>

    <!-- PASSWORD SCREEN -->
    <div id="password-screen">
        <p class="hint">The code is our birthdays MM/DD then the day we meet all together:)</p>
        <p>✨ ⭐ 🌸 ⭐ ✨</p>
        <input type="password" id="code-input" placeholder="Enter code..." onkeydown="if(event.key==='Enter') checkCode()">
        <br>
        <button class="btn-unlock" onclick="checkCode()">Open Letters 💌</button>
        <p id="error-msg">Incorrect code, try again structural setup my love! 💕</p>
    </div>

    <!-- MAIN WEBSITE CONTENT -->
    <div id="main-content">
        <h1 class="title-banner">✨ ⭐ Sonja's Open When Letters ⭐ ✨</h1>
        <div class="lily-deco">💮 🪷 💮 🪷</div>
        <p>Pick how you are feeling right now, my beautiful girl:</p>

        <!-- Emotion Buttons Grid -->
        <div class="grid">
            <button class="mood-btn" onclick="openLetter('sad')">😢 You're Sad</button>
            <button class="mood-btn" onclick="openLetter('happy')">☀️ You're Happy</button>
            <button class="mood-btn" onclick="openLetter('excited')">🎉 You're Excited</button>
            <button class="mood-btn" onclick="openLetter('upset-me')">😤 Upset At Me</button>
            <button class="mood-btn" onclick="openLetter('mad-others')">😡 Mad At Someone</button>
            <button class="mood-btn" onclick="openLetter('stressed')">🤯 Overwhelmed</button>
            <button class="mood-btn" onclick="openLetter('doubtful')">🧸 Feeling Doubtful</button>
            <button class="mood-btn" onclick="openLetter('motivation')">🔋 Lacking Motivation</button>
            <button class="mood-btn" onclick="openLetter('exam')">📚 Big Exam / Huge Thing</button>
            <button class="mood-btn" onclick="openLetter('random')">🎲 Open Randomly</button>
        </div>

        <!-- The Pink Paper Note Component -->
        <div id="letter-box">
            <h2 id="letter-title"></h2>
            <div id="letter-content"></div>
            <p style="text-align: right; margin-top: 20px; color: #ff4d6d; font-weight: bold;">✨ Forever Yours ✨</p>
        </div>
        
        <div class="lily-deco" style="margin-top: 40px;">🪷 ⭐ ✨ ⭐ 🪷</div>
    </div>

    <script>
        // Password Protection Logic
        function checkCode() {
            const input = document.getElementById('code-input').value;
            const correctCode = "032509040920";
            
            if (input === correctCode) {
                document.getElementById('password-screen').style.display = 'none';
                document.getElementById('main-content').style.display = 'block';
            } else {
                const error = document.getElementById('error-msg');
                error.style.display = 'block';
                // Quick reset animation hook
                error.style.animation = 'none';
                error.offsetHeight; 
                error.style.animation = null;
            }
        }

        // Database of your exact custom text letters
        const letters = {
            'sad': { 
                title: '✉️ Open when you\'re sad:', 
                content: 'Remember how you almost drowned at beach, and I told you to stand up, MIND YOU still afloat, yet scared the pooh out of me. ( Hoped you laughed and not made a face.Lol.) \n\nSeriously, just call me and we can add some joy to that blue mfker from insideout. :)' 
            },
            'happy': { 
                title: '✉️ Open when you\'re happy:', 
                content: 'Seeing you happy is amazing and heartwarming to me. I like you\'re smile, and just you Sonja. So, whatever is making you happy to open this, I want you to know your joy brings me additional joy. Keep shining and keep completing your goals.' 
            },
            'excited': { 
                title: '✉️ Open when you\'re excited:', 
                content: 'Whatever just happened, I know you worked hard for it and 101% deserve it.' 
            },
            'upset-me': { 
                title: '✉️ Open when you\'re upset at me:', 
                content: 'I probably overreacted, but maybe I am just as dramatic as you are, but... I will always communicate with you on everything. My frustration brings me alot of overwhelming emotions and I tend to get overly emotional. Knowing this makes me what to become more considerate about what I say and how I react. I am only improving everyday. \n\nNow text me, after we had our lil min apart to talk and fix our conflicted feelings.' 
            },
            'mad-others': { 
                title: '✉️ Open when you\'re mad at someone else:', 
                content: 'First off, you\'re 100% right, ans they are just 100% incomprehensive. Do not let others frustrate you or have control over how you react. That was always the goal to make you react. Do not let them accomplish, and don\'t let them rent space in your head. Take a deep breath, and remember that you are a total badass. \n\nAlso, you can always vent to me, but if I cannot respond in time, here\'s the letter to read for quicker reassurance.' 
            },
            'stressed': { 
                title: '✉️ Open when you\'re stressed or overwhelmed:', 
