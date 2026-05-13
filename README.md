# WebDeveloper
<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Developer Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #050505;
            --card-bg: #0d0d12;
            --primary-purple: #7c3aed;
            --text-main: #ffffff;
            --text-muted: #a1a1aa;
            --border-color: #1f1f23;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            font-family: 'Inter', sans-serif;
            margin: 0;
            line-height: 1.6;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 10%;
            background: rgba(5, 5, 5, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo { font-weight: 700; font-size: 1.2rem; display: flex; align-items: center; gap: 10px; }
        .logo span { color: var(--primary-purple); border: 2px solid; padding: 2px 6px; border-radius: 4px; }

        .nav-links { display: flex; gap: 25px; list-style: none; }
        .nav-links a { text-decoration: none; color: var(--text-muted); font-size: 0.9rem; transition: 0.3s; }
        .nav-links a:hover, .nav-links a.active { color: white; background: rgba(124, 58, 237, 0.2); padding: 5px 15px; border-radius: 20px; }

        .login-btn { border: 1px solid var(--primary-purple); padding: 8px 20px; border-radius: 20px; color: white; text-decoration: none; font-size: 0.9rem; }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 100px 10%;
            background: radial-gradient(circle at top, rgba(124, 58, 237, 0.15) 0%, transparent 70%);
        }

        .badge { background: rgba(124, 58, 237, 0.1); color: var(--primary-purple); padding: 5px 15px; border-radius: 20px; font-size: 0.7rem; text-transform: uppercase; letter-spacing: 1px; }

        h1 { font-size: 4rem; margin: 20px 0; background: linear-gradient(to bottom, #fff, #a78bfa); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        
        .hero p { color: var(--text-muted); max-width: 600px; margin: 0 auto 30px; }

        .btn-group { display: flex; justify-content: center; gap: 15px; }
        .btn-primary { background: var(--primary-purple); color: white; padding: 12px 30px; border-radius: 25px; text-decoration: none; font-weight: 600; }
        .btn-secondary { border: 1px solid var(--text-muted); color: white; padding: 12px 30px; border-radius: 25px; text-decoration: none; }

        /* Portfolio Filter */
        .portfolio-section { padding: 80px 10%; text-align: center; }
        .filter-buttons { display: flex; justify-content: center; gap: 10px; margin: 40px 0; flex-wrap: wrap; }
        .filter-btn { background: #1a1a1e; border: none; color: var(--text-muted); padding: 8px 18px; border-radius: 20px; cursor: pointer; transition: 0.3s; }
        .filter-btn.active { background: var(--primary-purple); color: white; }

        /* Grid Layout */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }

        .card {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 15px;
            overflow: hidden;
            text-align: left;
            transition: transform 0.3s;
        }

        .card:hover { transform: translateY(-5px); border-color: var(--primary-purple); }

        .card-img { width: 100%; height: 200px; background-size: cover; background-position: center; }

        .card-content { padding: 20px; }
        .card-title { font-size: 1.1rem; margin-bottom: 10px; }
        .card-link { color: var(--primary-purple); text-decoration: none; font-size: 0.85rem; float: right; }
        .card-tag { background: #1a1a1e; padding: 3px 10px; border-radius: 5px; font-size: 0.7rem; color: var(--text-muted); }

        /* Stats Section */
        .stats {
            background: #0a0a0f;
            display: flex;
            justify-content: space-around;
            padding: 40px 10%;
            border-radius: 20px;
            margin: 50px 10%;
            border: 1px solid var(--border-color);
        }

        .stat-item { text-align: center; }
        .stat-number { font-size: 2rem; font-weight: 700; display: block; }
        .stat-label { color: var(--text-muted); font-size: 0.8rem; }

        /* Footer CTA */
        .cta-footer { text-align: center; padding: 100px 10%; }
        .cta-footer h2 { font-size: 2.5rem; margin-bottom: 20px; }
        .cta-footer h2 span { color: var(--primary-purple); }

    </style>
</head>
<body>

    <nav>
        <div class="logo"><span>W</span> Web Developer</div>
        <ul class="nav-links">
            <li><a href="#" class="active">Home</a></li>
            <li><a href="#">Proiecte</a></li>
            <li><a href="#">Servicii</a></li>
            <li><a href="#">Despre Noi</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
        <a href="#" class="login-btn">Login 👤</a>
    </nav>

    <header class="hero">
        <span class="badge">Creăm experiențe digitale incredibile</span>
        <h1>Web Developer</h1>
        <p>Transformăm ideile tale în realitate digitală. Creăm site-uri moderne, rapide și intuitive pentru afacerea ta.</p>
        <div class="btn-group">
            <a href="#" class="btn-primary">Vezi Proiectele →</a>
            <a href="#" class="btn-secondary">Contactează-ne →</a>
        </div>
    </header>

    <section class="portfolio-section">
        <span class="badge">Alege soluția potrivită pentru tine</span>
        <h2 style="font-size: 2.5rem; margin-top: 15px;">Dorești un <span>website</span> sau cauți idei<br>pentru compania ta?</h2>
        
        <div class="filter-buttons">
            <button class="filter-btn active">Toate</button>
            <button class="filter-btn">Restaurante</button>
            <button class="filter-btn">Magazine Online</button>
            <button class="filter-btn">Portofolii</button>
            <button class="filter-btn">Hoteluri</button>
            <button class="filter-btn">Companii</button>
            <button class="filter-btn">Altele</button>
        </div>

        <div class="grid">
            <!-- Card 1 -->
            <div class="card">
                <div class="card-img" style="background-image: url('https://via.placeholder.com/400x250/1a1a1a/7c3aed?text=Restaurant+Gourmet')"></div>
                <div class="card-content">
                    <a href="#" class="card-link">Vezi exemplul →</a>
                    <div class="card-title">Restaurant Gourmet</div>
                    <span class="card-tag">Restaurante</span>
                </div>
            </div>
            <!-- Card 2 (Fashion) -->
            <div class="card" style="border-color: var(--primary-purple);">
                <div class="card-img" style="background-image: url('https://via.placeholder.com/400x250/1a1a1a/7c3aed?text=Fashion+Store')"></div>
                <div class="card-content">
                    <a href="#" class="card-link">Vezi exemplul →</a>
                    <div class="card-title">Fashion Store</div>
                    <span class="card-tag">Magazine Online</span>
                </div>
            </div>
            <!-- Card 3 -->
            <div class="card">
                <div class="card-img" style="background-image: url('https://via.placeholder.com/400x250/1a1a1a/7c3aed?text=Hotel+Royal')"></div>
                <div class="card-content">
                    <a href="#" class="card-link">Vezi exemplul →</a>
                    <div class="card-title">Hotel Royal</div>
                    <span class="card-tag">Hoteluri</span>
                </div>
            </div>
        </div>

        <a href="#" class="btn-secondary" style="font-size: 0.9rem;">Vezi toate proiectele →</a>
    </section>

    <div class="stats">
        <div class="stat-item">
            <span class="stat-number">50+</span>
            <span class="stat-label">Proiecte Finalizate</span>
        </div>
        <div class="stat-item">
            <span class="stat-number">30+</span>
            <span class="stat-label">Clienți Fericiți</span>
        </div>
        <div class="stat-item">
            <span class="stat-number">5+</span>
            <span class="stat-label">Ani Experiență</span>
        </div>
        <div class="stat-item">
            <span class="stat-number">24/7</span>
            <span class="stat-label">Suport Dedicat</span>
        </div>
    </div>

    <section class="cta-footer">
        <h2>Hai să construim ceva<br><span>incredibil împreună!</span></h2>
        <p style="color: var(--text-muted); margin-bottom: 30px;">Spune-ne despre proiectul tău și îți vom oferi cea mai bună soluție.</p>
        <a href="#" class="btn-primary" style="padding: 15px 50px;">Contactează-ne acum →</a>
    </section>

</body>
</html>
