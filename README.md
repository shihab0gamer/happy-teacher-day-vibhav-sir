<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Teacher's Day - Vaibhav Sir</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: white;
            padding: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .main-title {
            font-size: 2.8rem;
            margin-bottom: 10px;
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .dear-sir {
            font-size: 2rem;
            margin-bottom: 15px;
            color: #feca57;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.3);
        }

        .subtitle {
            font-size: 1.2rem;
            margin-bottom: 10px;
            opacity: 0.9;
        }

        .credit {
            font-size: 1rem;
            margin-bottom: 30px;
            opacity: 0.8;
            background: rgba(255,255,255,0.1);
            padding: 10px 20px;
            border-radius: 20px;
            display: inline-block;
        }

        .music-btn {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(255,255,255,0.2);
            border: none;
            padding: 15px;
            border-radius: 50%;
            cursor: pointer;
            font-size: 1.5rem;
            color: white;
            transition: all 0.3s ease;
        }

        .music-btn:hover {
            background: rgba(255,255,255,0.3);
            transform: scale(1.1);
        }

        .progress-container {
            margin: 30px 0;
        }

        .progress-text {
            font-size: 1.1rem;
            margin-bottom: 10px;
            opacity: 0.9;
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: rgba(255,255,255,0.3);
            border-radius: 4px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #00d2ff, #3a7bd5);
            width: 0%;
            transition: width 0.5s ease;
        }

        .puzzle-container {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px 30px;
            margin: 30px 0;
            box-shadow: 0 8px 32px rgba(0,0,0,0.2);
            border: 1px solid rgba(255,255,255,0.2);
        }

        .puzzle {
            display: none;
        }

        .puzzle.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .question-number {
            font-size: 1.1rem;
            color: #feca57;
            margin-bottom: 15px;
        }

        .question {
            font-size: 1.4rem;
            margin-bottom: 25px;
            line-height: 1.5;
        }

        .math-expression {
            font-size: 2.2rem;
            font-family: 'Courier New', monospace;
            background: rgba(255,255,255,0.2);
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
            display: inline-block;
            min-width: 200px;
        }

        .input-container {
            margin: 30px 0;
        }

        input[type="number"] {
            font-size: 1.8rem;
            padding: 15px 25px;
            border: none;
            border-radius: 15px;
            background: white;
            color: #333;
            width: 180px;
            text-align: center;
            margin: 0 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        input[type="number"]:focus {
            outline: none;
            box-shadow: 0 4px 20px rgba(254,202,87,0.5);
            transform: translateY(-2px);
        }

        .submit-btn {
            font-size: 1.3rem;
            padding: 15px 40px;
            background: linear-gradient(45deg, #ff6b6b, #ee5a24);
            color: white;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            margin-top: 20px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .submit-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
        }

        .hint {
            font-size: 1rem;
            color: #feca57;
            margin-top: 20px;
            font-style: italic;
            opacity: 0.8;
        }

        .message {
            background: linear-gradient(135deg, #feca57, #ff9ff3);
            padding: 25px;
            border-radius: 15px;
            margin: 25px 0;
            color: #333;
            font-size: 1.1rem;
            box-shadow: 0 6px 20px rgba(0,0,0,0.2);
            animation: slideIn 0.5s ease;
        }

        @keyframes slideIn {
            from { transform: translateX(-50px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }

        .final-message {
            background: linear-gradient(135deg, #667eea, #764ba2);
            border: 3px solid gold;
            padding: 40px;
            border-radius: 20px;
            font-size: 1.2rem;
            line-height: 1.6;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            margin: 30px 0;
        }

        .error-message {
            background: linear-gradient(135deg, #ff6b6b, #ee5a24);
            color: white;
        }

        .success-icon {
            font-size: 2rem;
            margin-bottom: 15px;
            display: block;
        }

        /* Enhanced animations for innovative effects */
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }
        
        @keyframes colorWave {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        @keyframes explode {
            0% { 
                transform: translate(-50%, -50%) scale(0) rotate(0deg); 
                opacity: 1; 
            }
            100% { 
                transform: translate(
                    calc(-50% + ${Math.random() * 200 - 100}px), 
                    calc(-50% + ${Math.random() * 200 - 100}px)
                ) scale(1) rotate(360deg); 
                opacity: 0; 
            }
        }
        
        @keyframes errorBurst {
            0% { 
                transform: scale(1); 
                opacity: 1; 
            }
            100% { 
                transform: scale(0) translate(${Math.random() * 100 - 50}px, ${Math.random() * 100 - 50}px); 
                opacity: 0; 
            }
        }
        
        /* Enhanced device compatibility */
        @media (max-width: 1024px) {
            .main-title { font-size: 2.5rem; }
            .dear-sir { font-size: 1.8rem; }
        }

        @media (max-width: 768px) {
            .main-title { font-size: 2.2rem; }
            .dear-sir { font-size: 1.6rem; }
            .subtitle { font-size: 1rem; }
            .puzzle-container { padding: 25px 20px; }
            .math-expression { font-size: 1.8rem; padding: 15px; }
            input[type="number"] { font-size: 1.5rem; width: 150px; }
            .submit-btn { padding: 12px 30px; font-size: 1.1rem; }
        }

        @media (max-width: 600px) {
            .container { padding: 15px; }
            .main-title { font-size: 2rem; }
            .dear-sir { font-size: 1.4rem; }
            .puzzle-container { padding: 20px 15px; margin: 20px 0; }
            .math-expression { font-size: 1.6rem; }
            input[type="number"] { width: 140px; font-size: 1.4rem; }
        }

        @media (max-width: 480px) {
            .main-title { font-size: 1.8rem; }
            .dear-sir { font-size: 1.3rem; }
            .subtitle { font-size: 0.9rem; }
            .math-expression { font-size: 1.5rem; padding: 12px; }
            input[type="number"] { width: 120px; font-size: 1.3rem; padding: 12px 20px; }
            .submit-btn { padding: 10px 25px; font-size: 1rem; }
            .puzzle-container { padding: 18px 12px; }
            .music-btn { top: 15px; right: 15px; padding: 12px; }
        }

        @media (max-width: 380px) {
            .main-title { font-size: 1.6rem; }
            .dear-sir { font-size: 1.2rem; }
            .credit { font-size: 0.9rem; padding: 8px 16px; }
            .math-expression { font-size: 1.3rem; }
            input[type="number"] { width: 110px; font-size: 1.2rem; }
        }
        
        /* Landscape orientation fixes */
        @media (max-height: 500px) and (orientation: landscape) {
            .main-title { font-size: 1.5rem; margin-bottom: 5px; }
            .dear-sir { font-size: 1.2rem; margin-bottom: 5px; }
            .subtitle { font-size: 0.9rem; margin-bottom: 5px; }
            .credit { font-size: 0.8rem; margin-bottom: 15px; }
            .puzzle-container { padding: 15px; margin: 15px 0; }
            .progress-container { margin: 15px 0; }
        }
        
        /* High DPI displays */
        @media (-webkit-min-device-pixel-ratio: 2), (min-resolution: 192dpi) {
            .math-expression {
                -webkit-font-smoothing: antialiased;
                -moz-osx-font-smoothing: grayscale;
            }
        }
        
        /* Touch device optimizations */
        @media (hover: none) and (pointer: coarse) {
            .submit-btn {
                min-height: 44px;
                min-width: 44px;
            }
            
            input[type="number"] {
                min-height: 44px;
                font-size: 16px; /* Prevents zoom on iOS */
            }
            
            .music-btn {
                min-height: 44px;
                min-width: 44px;
            }
        }
        
        /* Dark mode support */
        @media (prefers-color-scheme: dark) {
            body {
                background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            }
        }
        
        /* Reduced motion for accessibility */
        @media (prefers-reduced-motion: reduce) {
            * {
                animation-duration: 0.01ms !important;
                animation-iteration-count: 1 !important;
                transition-duration: 0.01ms !important;
            }
        }
    </style>
</head>
<body>
    <div class="music-btn" onclick="toggleMusic()">
        <span id="musicIcon">🎵</span>
    </div>

    <div class="container">
        <h1 class="main-title">🎉 Happy Teacher's Day! 🎉</h1>
        <div class="dear-sir">Dear <u>Vaibhav Sir</u></div>
        <div class="subtitle">A Special Mathematical Journey For You</div>
        <div class="credit">
            Made with ❤ by <u>SHIHAB</u> from <u>HUBLI</u> Pathshala
        </div>
        
        <div class="progress-container">
            <div class="progress-text">Progress: <span id="progressText">1 of 5</span></div>
            <div class="progress-bar">
                <div class="progress-fill" id="progressBar"></div>
            </div>
        </div>

        <!-- Puzzle 1: Basic Algebra -->
        <div class="puzzle active" id="puzzle1">
            <div class="puzzle-container">
                <div class="question-number">Question 1 of 5</div>
                <div class="question">🔢 Let's start with basic algebra!</div>
                <div class="math-expression">2x + 5 = 17</div>
                <div class="input-container">
                    <div style="margin-bottom: 15px;">What is the value of x?</div>
                    <input type="number" id="answer1" placeholder="Enter x">
                    <br>
                    <button class="submit-btn" onclick="checkAnswer(1, 6)">Submit Answer</button>
                </div>
                <div class="hint">💡 Hint: Subtract 5 from both sides, then divide by 2</div>
            </div>
        </div>

        <!-- Puzzle 2: Quadratic Equation -->
        <div class="puzzle" id="puzzle2">
            <div class="puzzle-container">
                <div class="question-number">Question 2 of 5</div>
                <div class="question">📐 Now let's solve a quadratic equation!</div>
                <div class="math-expression">x² - 7x + 12 = 0</div>
                <div class="input-container">
                    <div style="margin-bottom: 15px;">What is the smaller positive root?</div>
                    <input type="number" id="answer2" placeholder="Enter x">
                    <br>
                    <button class="submit-btn" onclick="checkAnswer(2, 3)">Submit Answer</button>
                </div>
                <div class="hint">💡 Hint: Try factoring into (x - ?)(x - ?) = 0</div>
            </div>
        </div>

        <!-- Puzzle 3: Trigonometry -->
        <div class="puzzle" id="puzzle3">
            <div class="puzzle-container">
                <div class="question-number">Question 3 of 5</div>
                <div class="question">📊 Time for trigonometry!</div>
                <div class="math-expression">sin(30°) × 12 = ?</div>
                <div class="input-container">
                    <div style="margin-bottom: 15px;">Calculate the result</div>
                    <input type="number" id="answer3" placeholder="Enter result">
                    <br>
                    <button class="submit-btn" onclick="checkAnswer(3, 6)">Submit Answer</button>
                </div>
                <div class="hint">💡 Hint: sin(30°) = 0.5, so 0.5 × 12 = ?</div>
            </div>
        </div>

        <!-- Puzzle 4: Geometry -->
        <div class="puzzle" id="puzzle4">
            <div class="puzzle-container">
                <div class="question-number">Question 4 of 5</div>
                <div class="question">🔺 Let's explore geometry!</div>
                <div class="math-expression">Area = ½ × 8 × 6</div>
                <div class="input-container">
                    <div style="margin-bottom: 15px;">What is the area of this triangle?</div>
                    <input type="number" id="answer4" placeholder="Enter area">
                    <br>
                    <button class="submit-btn" onclick="checkAnswer(4, 24)">Submit Answer</button>
                </div>
                <div class="hint">💡 Hint: ½ × 8 × 6 = 4 × 6 = ?</div>
            </div>
        </div>

        <!-- Puzzle 5: Calculus -->
        <div class="puzzle" id="puzzle5">
            <div class="puzzle-container">
                <div class="question-number">Question 5 of 5</div>
                <div class="question">📈 Finally, basic calculus!</div>
                <div class="math-expression">d/dx (3x²) = ?x</div>
                <div class="input-container">
                    <div style="margin-bottom: 15px;">What coefficient replaces the ?</div>
                    <input type="number" id="answer5" placeholder="Enter coefficient">
                    <br>
                    <button class="submit-btn" onclick="checkAnswer(5, 6)">Submit Answer</button>
                </div>
                <div class="hint">💡 Hint: Use power rule: d/dx(3x²) = 3 × 2 × x¹ = 6x</div>
            </div>
        </div>

        <!-- Final Message Container -->
        <div id="finalMessage" style="display: none;">
            <div class="final-message">
                <div id="revealedMessage"></div>
            </div>
        </div>

        <!-- Messages container -->
        <div id="messageContainer"></div>
    </div>

    <!-- Simple Audio for music -->
    <audio id="bgMusic" loop style="display: none;">
        <!-- We'll create simple tones with JavaScript -->
    </audio>

    <script>
        let currentPuzzle = 1;
        const totalPuzzles = 5;
        let musicPlaying = false;
        let audioContext = null;
        let musicInterval = null;

        const mathQuotes = [
            "🎯 'Mathematics is the language with which God has written the universe.' - Galileo",
            "🚀 'Mathematics is not about numbers, equations, or algorithms: it is about understanding.' - Thurston",
            "🌟 'Pure mathematics is, in its way, the poetry of logical ideas.' - Einstein",
            "💎 'Mathematics is the most beautiful creation of the human spirit.' - Banach",
            "✨ 'In mathematics, you don't understand things. You just get used to them.' - von Neumann"
        ];

        function updateProgress() {
            const progress = ((currentPuzzle - 1) / totalPuzzles) * 100;
            document.getElementById('progressBar').style.width = progress + '%';
            document.getElementById('progressText').textContent = ${currentPuzzle - 1} of ${totalPuzzles};
        }

        function checkAnswer(puzzleNum, correctAnswer) {
            const userInput = document.getElementById('answer' + puzzleNum);
            const userAnswer = parseFloat(userInput.value);
            
            // Clear previous messages
            const existingMessages = document.querySelectorAll('.message');
            existingMessages.forEach(msg => msg.remove());
            
            if (userAnswer === correctAnswer) {
                // Play success sound
                playSuccessSound();
                
                // Correct answer
                const messageDiv = document.createElement('div');
                messageDiv.className = 'message';
                messageDiv.innerHTML = `
                    <span class="success-icon">✅</span>
                    <div style="font-size: 1.2rem; margin-bottom: 10px; font-weight: bold;">Excellent work!</div>
                    <div style="font-size: 1rem; font-style: italic; line-height: 1.4;">
                        ${mathQuotes[puzzleNum - 1]}
                    </div>
                `;
                
                document.getElementById('messageContainer').appendChild(messageDiv);
                
                // Create success particle effect
                createSuccessParticles();
                
                // Move to next puzzle
                setTimeout(() => {
                    document.getElementById('puzzle' + puzzleNum).classList.remove('active');
                    
                    if (currentPuzzle < totalPuzzles) {
                        currentPuzzle++;
                        document.getElementById('puzzle' + currentPuzzle).classList.add('active');
                        updateProgress();
                        
                        // Scroll to top on mobile
                        window.scrollTo({top: 0, behavior: 'smooth'});
                    } else {
                        showFinalMessage();
                    }
                }, 2500);
                
            } else {
                // Play error sound - innovative multi-tone error sound
                playInnovativeErrorSound();
                
                // Create screen shake effect
                document.body.style.animation = 'shake 0.5s ease-in-out';
                setTimeout(() => {
                    document.body.style.animation = '';
                }, 500);
                
                // Wrong answer with innovative visual feedback
                const messageDiv = document.createElement('div');
                messageDiv.className = 'message error-message';
