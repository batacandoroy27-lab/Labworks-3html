
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Interactive Profile Card</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <main class="profile-card">

        <div class="badge">✨ MY PROFILE ✨</div>

        <!-- Image Placeholder -->
        <div class="profile-image">
            <span>🌷</span>
            <p>My Profile Picture</p>
        </div>

        <h1>Hi, I'm Ryn! 💕</h1>

        <p class="subtitle">
            Student | Future Web Developer
        </p>

        <p class="description">
            Hello! Welcome to my little corner of the internet! 🌷
            I enjoy learning new things, exploring technology,
            expressing my creativity, and creating beautiful
            websites using HTML and CSS.
        </p>

        <div class="divider"></div>

        <h2>🌸 My Skills 🌸</h2>

        <!-- Four skill items for nth-child() -->
      
<ul class="skills">
    <li>🎨 Drawing & Painting</li>
    <li>🎤 Singing</li>
    <li>🧠 Creative thinking</li>
    <li>💭 Analytical Skills</li>
    <li>🧩 Problem Solving</li>
    <li>😌 Pattern Recognition</li>
    <li>😶‍🌫️ Strategic Thinking</li>
    <li>💡 Imagination</li>
    <li>🚀 Creativity</li>
</ul>


        <div class="divider"></div>

        <h2>💌 Say Hello!</h2>

        <!-- Input with focus effect -->
        <label for="nickname">What's your name?</label>

        <input
            type="text"
            id="nickname"
            placeholder="Enter your name..."
        >

        <!-- Two interactive buttons -->
        <div class="button-group">
            <button type="button" id="helloBtn">
                💗 Say Hello
            </button>

            <button type="button" id="themeBtn">
                🌙 Change Theme
            </button>
        </div>

        <p id="message" role="status" aria-live="polite"></p>

        <footer>
            💗✨ Never give up. Great things take time,
            and every small step brings you closer to your dreams. 💗✨
            <br>
            <span>Dream big, stay creative! 🌷</span>
        </footer>

    </main>

    <script>
        const helloBtn = document.getElementById("helloBtn");
        const themeBtn = document.getElementById("themeBtn");
        const nickname = document.getElementById("nickname");
        const message = document.getElementById("message");

        // Button 1: Say Hello
        helloBtn.addEventListener("click", function () {
            const name = nickname.value.trim() || "Friend";

            message.textContent =
                "Hello, " + name + "! Welcome to my profile! 🎉💗";
        });

        // Button 2: Change Theme
        themeBtn.addEventListener("click", function () {
            document.body.classList.toggle("alternate-theme");

            if (document.body.classList.contains("alternate-theme")) {
                themeBtn.textContent = "🌸 Pink Theme";
            } else {
                themeBtn.textContent = "🌙 Change Theme";
            }
        });
    </script>

</body>
</html>
