<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Babyyy ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .container {
            text-align: center;
            position: relative;
            width: 100%;
            max-width: 500px;
            padding: 20px;
        }

        /* Floating Hearts Animation */
        .heart {
            position: absolute;
            color: #ff69b4;
            font-size: 20px;
            animation: float 6s ease-in-out infinite;
            opacity: 0.7;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        .heart:nth-child(1) { top: 10%; left: 10%; animation-delay: 0s; }
        .heart:nth-child(2) { top: 20%; right: 10%; animation-delay: 2s; }
        .heart:nth-child(3) { bottom: 30%; left: 20%; animation-delay: 4s; }
        .heart:nth-child(4) { bottom: 20%; right: 20%; animation-delay: 1s; }
        .heart:nth-child(5) { top: 50%; left: 5%; animation-delay: 3s; }
        .heart:nth-child(6) { top: 40%; right: 5%; animation-delay: 5s; }

        /* Mystery Box Styles */
        .mystery-box {
            width: 200px;
            height: 200px;
            background: linear-gradient(45deg, #ff1744, #e91e63);
            border-radius: 20px;
            margin: 0 auto 30px;
            position: relative;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(233, 30, 99, 0.4);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        .mystery-box:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 40px rgba(233, 30, 99, 0.6);
        }

        .mystery-box::before {
            content: '?';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-size: 80px;
            color: white;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .ribbon {
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 220px;
            background: #ffd700;
            border-radius: 5px;
            box-shadow: 0 2px 10px rgba(255, 215, 0, 0.5);
        }

        .ribbon::after {
            content: '';
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 60px;
            background: #ffd700;
            border-radius: 50%;
            box-shadow: 0 2px 10px rgba(255, 215, 0, 0.5);
        }

        /* Birthday Message Styles */
        .birthday-message {
            display: none;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .birthday-text {
            font-size: 48px;
            color: #e91e63;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            font-weight: bold;
        }

        .name-text {
            font-size: 36px;
            color: #ff1744;
            margin-bottom: 30px;
            font-style: italic;
        }

        .love-button {
            background: linear-gradient(45deg, #e91e63, #ff1744);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 18px;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(233, 30, 99, 0.4);
            font-family: 'Georgia', serif;
            font-weight: bold;
        }

        .love-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(233, 30, 99, 0.6);
        }

        /* Love Letter Styles */
        .love-letter {
            display: none;
            background: #fff;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            margin-top: 30px;
            position: relative;
            animation: fadeInUp 1s ease-out;
            max-height: 70vh;
            overflow-y: auto;
        }

        .love-letter::before {
            content: '💕';
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 30px;
            background: white;
            padding: 0 10px;
        }

        .letter-title {
            font-size: 24px;
            color: #e91e63;
            margin-bottom: 20px;
            text-align: center;
            font-weight: bold;
        }

        .letter-content {
            font-size: 16px;
            line-height: 1.8;
            color: #333;
            text-align: left;
        }

        .letter-signature {
            margin-top: 30px;
            text-align: right;
            font-style: italic;
            color: #e91e63;
            font-size: 18px;
        }

        .back-button {
            background: linear-gradient(45deg, #ff9a9e, #fecfef);
            color: #e91e63;
            border: none;
            padding: 10px 30px;
            font-size: 16px;
            border-radius: 25px;
            cursor: pointer;
            margin-top: 20px;
            transition: all 0.3s ease;
            font-family: 'Georgia', serif;
        }

        .back-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(233, 30, 99, 0.3);
        }

        /* Sparkle Animation */
        .sparkle {
            position: absolute;
            color: #ffd700;
            font-size: 16px;
            animation: sparkle 3s ease-in-out infinite;
            pointer-events: none;
        }

        @keyframes sparkle {
            0%, 100% { opacity: 0; transform: scale(0); }
            50% { opacity: 1; transform: scale(1); }
        }
    </style>
</head>
<body>
    <!-- Floating Hearts -->
    <div class="heart">💖</div>
    <div class="heart">💕</div>
    <div class="heart">💗</div>
    <div class="heart">💝</div>
    <div class="heart">💖</div>
    <div class="heart">💕</div>

    <div class="container">
        <!-- Mystery Box Section -->
        <div class="mystery-section" id="mysterySection">
            <div class="mystery-box" id="mysteryBox" onclick="openBox()">
                <div class="ribbon"></div>
            </div>
            <p style="color: #e91e63; font-size: 18px; margin-top: 20px;">CLICK ME, BABEE! 💕</p>
        </div>

        <!-- Birthday Message Section -->
        <div class="birthday-message" id="birthdayMessage">
            <div class="birthday-text">Happy Birthday🎉</div>
            <div class="birthday-text">To My Sweetest Boyfriend In The World!!!</div>
            <div class="name-text">-Saf! 💖</div>
            <button class="love-button" onclick="showLoveLetter()">💌 My Love Letter 💌</button>
        </div>

        <!-- Love Letter Section -->
<div class="love-letter" id="loveLetter">
    <div class="letter-title">💕 HBD Loveee 💕</div>
    <div class="letter-content">
        <p>My sweetesttt boyfriend ever Daizzz,</p>

        <p>I hope today wraps itself in warmth and wonder —<br>
        a truly special day,even if I’m someone who tends to forget the little things.</p>

        <p>Still, I could never forget <strong>you</strong>.</p>

        <p>May every dream that lives in your heart<br>
        begin to bloom like spring's first light.</p>

        <p>May health always stay beside you,<br>
        and joy find its way to you — again and again.</p>

        <p>I hope you’ll always carry the light to make yourself happy,<br>
        and that your smile continues<br>
        to brighten the lives around you.</p>

        <p>I hope our journey stays long —<br>
        as long as forever allows.💕</p>

        <p>And just so you know:<br>
        I’m so incredibly grateful we met,<br>
        so grateful we found our way<br>
        into each other’s lives — and hearts. 🌙⭐</p>

        <p>I may not be the best<br>
        at showing how I feel,<br>
        but I do love you —<br>
        so deeply,<br>
        so endlessly.💕</p>

        <p>I feel lucky every single day<br>
        because you exist in my world.💕</p>

        <p>I love you so, so much.💕<br>
        And I can't wait to build<br>
        more beautiful memories by your side.</p>

        <p>Happy birthday once again, baby. 🌹</p>
    </div>
    <div class="letter-signature">
        With all my love,<br>
        From your prettiest girlfriend,<br>
        Safira ❤️
    </div>
    <button class="back-button" onclick="backToBirthday()">💖 Back</button>
</div>
    </div>

    <script>
        // Create sparkles effect
        function createSparkle() {
            const sparkle = document.createElement('div');
            sparkle.className = 'sparkle';
            sparkle.innerHTML = '✨';
            sparkle.style.left = Math.random() * 100 + 'vw';
            sparkle.style.top = Math.random() * 100 + 'vh';
            document.body.appendChild(sparkle);
            
            setTimeout(() => {
                sparkle.remove();
            }, 3000);
        }

        // Create sparkles periodically
        setInterval(createSparkle, 1000);

        function openBox() {
            const mysterySection = document.getElementById('mysterySection');
            const birthdayMessage = document.getElementById('birthdayMessage');
            
            // Add sparkle effect on click
            for(let i = 0; i < 10; i++) {
                setTimeout(() => createSparkle(), i * 100);
            }
            
            // Hide mystery box and show birthday message
            mysterySection.style.display = 'none';
            birthdayMessage.style.display = 'block';
        }

        function showLoveLetter() {
            const birthdayMessage = document.getElementById('birthdayMessage');
            const loveLetter = document.getElementById('loveLetter');
            
            birthdayMessage.style.display = 'none';
            loveLetter.style.display = 'block';
        }

        function backToBirthday() {
            const birthdayMessage = document.getElementById('birthdayMessage');
            const loveLetter = document.getElementById('loveLetter');
            
            loveLetter.style.display = 'none';
            birthdayMessage.style.display = 'block';
        }
    </script>
</body>
</html>
