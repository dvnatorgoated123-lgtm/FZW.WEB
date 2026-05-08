<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FuzionWorks | Roblox Game Studio</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #050505;
            --text-color: #ffffff;
            --accent-color: #00a2ff;
            --card-bg: #151515;
        }

        body {
            margin: 0;
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            scroll-behavior: smooth;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 5%;
            position: fixed;
            width: 90%;
            top: 0;
            background: rgba(5, 5, 5, 0.8);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid #222;
        }

        /* Logo Image Style */
        .logo img {
            height: 50px; /* Adjust height based on your logo design */
            cursor: pointer;
            transition: transform 0.3s;
        }
        .logo img:hover { transform: scale(1.05); }

        .nav-links a {
            color: white;
            text-decoration: none;
            margin-left: 25px;
            font-size: 0.9rem;
            font-weight: 600;
            transition: 0.3s;
        }
        .nav-links a:hover { color: var(--accent-color); }

        /* Hero with Background Video */
        .hero {
            position: relative;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            overflow: hidden; /* Keeps video inside container */
            padding: 0 5%;
        }

        #hero-video {
            position: absolute;
            top: 50%;
            left: 50%;
            min-width: 100%;
            min-height: 100%;
            width: auto;
            height: auto;
            z-index: -2;
            transform: translate(-50%, -50%);
            object-fit: cover;
        }

        /* Dark overlay so text is readable over video */
        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            z-index: -1;
        }

        .hero h1 { font-size: 5rem; margin: 0; text-transform: uppercase; letter-spacing: 2px; }
        .hero p { font-size: 1.2rem; color: #eee; max-width: 600px; margin-bottom: 30px; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }

        /* Games Section */
        #games { padding: 80px 5%; }
        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .game-card {
            background: var(--card-bg);
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid #333;
            transition: 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .game-card:hover { transform: scale(1.03); border-color: var(--accent-color); }
        .game-thumb { width: 100%; height: 200px; object-fit: cover; }
        .game-info { padding: 20px; }
        .game-info h3 { margin: 0; font-size: 1.4rem; }

        /* Form */
        #contact { padding: 100px 5%; background: #0a0a0a; text-align: center; }
        .contact-container { max-width: 600px; margin: 0 auto; text-align: left; }
        
        input, textarea {
            width: 100%;
            padding: 15px;
            margin: 10px 0;
            background: #1a1a1a;
            border: 1px solid #333;
            color: white;
            border-radius: 8px;
            box-sizing: border-box;
        }

        .btn {
            background: var(--accent-color);
            color: black;
            padding: 15px 35px;
            border: none;
            border-radius: 8px;
            font-weight: 800;
            cursor: pointer;
            width: 100%;
            transition: 0.3s;
        }
        .btn:hover { opacity: 0.8; transform: translateY(-2px); }

        footer { padding: 40px; text-align: center; border-top: 1px solid #222; color: #555; }
    </style>
</head>
<body>

    <nav>
        <div class="logo" onclick="window.scrollTo(0,0)">
            <img src="https://via.placeholder.com/200x60?text=FUZION+LOGO" alt="FuzionWorks Logo">
        </div>
        <div class="nav-links">
            <a href="#games">Games</a>
            <a href="#contact">Acquisition</a>
            <a href="https://www.roblox.com" target="_blank">Roblox Group</a>
        </div>
    </nav>

    <section class="hero">
        <video autoplay muted loop playsinline id="hero-video">
            <source src="https://www.w3schools.com/howto/rain.mp4" type="video/mp4">
        </video>
        <div class="hero-overlay"></div>

        <h1>FUZIONWORKS</h1>
        <p>The next generation of immersive Roblox experiences. We build, acquire, and scale top-tier games.</p>
        <button class="btn" style="width: auto;" onclick="document.getElementById('games').scrollIntoView()">View Our Portfolio</button>
    </section>

    <section id="games">
        <h2 style="font-size: 2.5rem;">Our Games</h2>
        <div class="games-grid">
            <div class="game-card">
                <img src="https://picsum.photos/id/1070/400/250" alt="Horror Game" class="game-thumb">
                <div class="game-info">
                    <h3>Hunted</h3>
                    <p>Horror/Assymetrical</p>
                    <button class="btn" onclick="window.open('https://www.roblox.com/games/108114165411484/HUNTED')">Play Now</button>
                </div>
            </div>
            <div class="game-card">
                <img src="https://picsum.photos/id/230/400/250" alt="Strategy Game" class="game-thumb">
                <div class="game-info">
                    <h3>Rushed</h3>
                    <p>Strategy/Minigame</p>
                    <button class="btn" onclick="window.open('https://www.roblox.com/games/132853089500750/Rushed')">Play Now</button>
                </div>
            </div>
            <div class="game-card">
                <img src="https://picsum.photos/id/382/400/250" alt="Soccer Game" class="game-thumb">
                <div class="game-info">
                    <h3>Head Football(coming soon)</h3>
                    <p>Sports/Action</p>
                    <button class="btn" onclick="window.open('https://www.roblox.com/games/105355041563819/Climb-Scary-Mrbeast-Tower')">Play Now</button>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="contact-container">
            <h2>Acquire Your Game</h2>
            <p>Fill out the form below to pitch your game for acquisition.</p>
            <form id="acquisitionForm">
                <input type="text" id="gameLink" placeholder="Roblox Game Link" required>
                <input type="email" id="email" placeholder="Your Discord or Email" required>
                <textarea id="metrics" rows="4" placeholder="Monthly Revenue & Active Users" required></textarea>
                <button type="submit" class="btn">Submit Pitch</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 FUZIONWORKS STUDIO. Not affiliated with Roblox Corp.</p>
    </footer>

    <script>
        // Form Handling
        document.getElementById('acquisitionForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const link = document.getElementById('gameLink').value;
            const contact = document.getElementById('email').value;
            if(link && contact) {
                alert(`Pitch received for: ${link}. We will contact you at ${contact}.`);
                this.reset();
            }
        });

        // Smooth scroll for nav links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
