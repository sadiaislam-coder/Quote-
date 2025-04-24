<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Lavender Inspiration</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background:url(https://wallpapers.com/images/high/light-purple-aesthetic-street-light-1oj1xspytai2zgur.webp)
      no-repeat center center fixed;
      background-size:cover;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .card {
      background-color: rgba(255, 255, 255, 0.7);
      border-radius: 20px;
      box-shadow: 0 0 30px rgba(0, 0, 0, 0.2);
      padding: 40px;
      max-width: 600px;
      text-align: center;
      backdrop-filter: blur(10px);
    }
    h1 {
      font-size: 32px;
      color: #4B0082;
    }
    #quote {
      font-size: 22px;
      font-style: italic;
      margin: 20px 0;
      color: #2F4F4F;
    }
    #author {
      font-size: 18px;
      color: #696969;
    }
    button {
      background-color: #B497BD;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      border-radius: 30px;
      cursor: pointer;
      margin-top: 20px;
      color: white;
      transition: background-color 0.3s;
    }
    button:hover {
      background-color: #9370DB;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Fuel Me with good Vibes</h1>
    <p id="quote">Click the button to get inspired!</p>
    <p id="author"></p>
    <button onclick="generateQuote(); playAudio()">🍁Inspire Me🍁</button>
  </div>

  <!-- Soothing background music -->
  <audio id="bg-music" src="https://www.chosic.com/wp-content/uploads/2021/02/PerituneMaterial_Sakuya2(chosic.com).mp3"></audio>

  <script>
    const quotes = [
      {
        quote: "The best way to predict the future is to invent it.",
        author: "— Alan Kay"
      },
      {
        quote: "Success is not final, failure is not fatal: It is the courage to continue that counts.",
        author: "— Winston Churchill"
      },
      {
        quote: "Be yourself; everyone else is already taken.",
        author: "— Oscar Wilde"
      },
      {
        quote: "Believe you can and you're halfway there.",
        author: "— Theodore Roosevelt"
      },
      {
        quote: "You must be the change you wish to see in the world.",
        author: "— Mahatma Gandhi"
      },
      {
        quote: "It does not matter how slowly you go as long as you do not stop.",
        author: "— Confucius"
      },
      {
        quote: "Your time is limited, don’t waste it living someone else’s life.",
        author: "— Steve Jobs"
      },
      {
        quote: "Happiness can be found even in the darkest of times, if one only remembers to turn on the light.",
        author: "— Albus Dumbledore"
      }
    ];

    function generateQuote() {
      const randomIndex = Math.floor(Math.random() * quotes.length);
      const quoteText = quotes[randomIndex];
      document.getElementById("quote").textContent = `"${quoteText.quote}"`;
      document.getElementById("author").textContent = quoteText.author;
    }

    function playAudio() {
      const audio = document.getElementById("bg-music");
      audio.volume = 0.2;
      audio.play();
    }
  </script>
</body>
</html>
