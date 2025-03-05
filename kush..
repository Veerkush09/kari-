<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Surprised</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #e0f7fa; /* हल्का नीला बैकग्राउंड */
            color: #333;
            position: relative;
            overflow: hidden; /* दिलों को बाहर जाने से रोकने के लिए */
        }
        h1 {
            font-size: 48px;
            color: #00796b; /* गहरा हरा रंग */
            margin-bottom: 20px;
        }
        button {
            margin: 10px;
            padding: 15px 30px;
            font-size: 20px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s, transform 0.3s;
        }
        #yesButton {
            background-color: #4caf50; /* हरा रंग */
            color: white;
        }
        #noButton {
            background-color: #f44336; /* लाल रंग */
            color: white;
            position: absolute;
        }
        button:hover {
            transform: scale(1.05);
        }
        #message {
            margin-top: 20px;
            font-size: 24px;
            color: #d32f2f;
            display: none;
            font-weight: bold;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: float 2s ease-in-out infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
        .watermark {
            position: absolute;
            bottom: 10px;
            right: 10px;
            font-size: 30px;
            color: rgba(0, 0, 0, 0.1);
            pointer-events: none;
        }
    </style>
</head>
<body>

    <h1>Surprised</h1>
    <button id="yesButton">Yes</button>
    <button id="noButton">No</button>
    <div id="message">I love you Kari ❤️</div>
    <div class="watermark">GoviKari</div>

    <script>
        const yesButton = document.getElementById('yesButton');
        const noButton = document.getElementById('noButton');
        const message = document.getElementById('message');

        // "Yes" बटन पर क्लिक करने पर दिल और मैसेज दिखेगा
        yesButton.addEventListener('click', function() {
            message.style.display = 'block';
            createHearts();
        });

        // "No" बटन माउस से भागेगा
        noButton.addEventListener('mouseover', function() {
            const randomX = Math.random() * (window.innerWidth - 100);
            const randomY = Math.random() * (window.innerHeight - 100);
            noButton.style.left = `${randomX}px`;
            noButton.style.top = `${randomY}px`;
        });

        // दिल बनाने वाला फंक्शन
        function createHearts() {
            for (let i = 0; i < 20; i++) { // 20 दिल बनाएंगे
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.innerHTML = '❤️';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.top = Math.random() * 100 + 'vh';
                heart.style.fontSize = Math.random() * 20 + 20 + 'px'; // साइज अलग-अलग होगा
                
                document.body.appendChild(heart);

                // 3 सेकंड बाद दिल गायब हो जाएगा
                setTimeout(() => {
                    heart.remove();
                }, 3000);
            }
        }
    </script>

</body>
</html>
