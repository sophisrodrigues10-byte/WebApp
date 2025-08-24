# WebApp
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>One Direction - Fan Experience</title>
    <meta name="description" content="Descubra a jornada, música e legado do One Direction. Estatísticas em tempo real, discografia completa e muito mais.">
    <link rel="stylesheet" href="styles.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Navigation -->
    <nav class="nav">
        <div class="nav-container">
            <div class="nav-brand">
                <h1>One Direction</h1>
            </div>
            <div class="nav-links">
                <a href="#hero" class="nav-link">Início</a>
                <a href="#members" class="nav-link">Banda</a>
                <a href="#music" class="nav-link">Música</a>
                <a href="#stats" class="nav-link">Estatísticas</a>
            </div>
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="hero" class="hero">
        <div class="hero-bg"></div>
        <div class="hero-content">
            <h1 class="hero-title">One Direction</h1>
            <p class="hero-subtitle">
                A banda britânico-irlandesa que conquistou o mundo. Descubra sua jornada, música e legado.
            </p>
            <div class="hero-buttons">
                <button class="btn btn-primary" onclick="scrollToSection('music')">
                    Explorar Música
                </button>
                <button class="btn btn-outline" onclick="scrollToSection('members')">
                    Conhecer a Banda
                </button>
            </div>
        </div>
        <div class="floating-elements">
            <div class="float-1"></div>
            <div class="float-2"></div>
            <div class="float-3"></div>
            <div class="float-4"></div>
        </div>
    </section>

    <!-- Band Members Section -->
    <section id="members" class="members">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">A Banda</h2>
                <p class="section-subtitle">
                    Cinco talentos individuais que se uniram para criar magia
                </p>
            </div>
            <div class="members-grid" id="membersGrid">
                <!-- Members will be loaded by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Music Section -->
    <section id="music" class="music">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Discografia</h2>
                <p class="section-subtitle">
                    Cinco álbuns de estúdio que definiram uma geração e conquistaram corações mundialmente
                </p>
            </div>
            <div class="albums-grid" id="albumsGrid">
                <!-- Albums will be loaded by JavaScript -->
            </div>
            
            <div class="section-header">
                <h3 class="section-title-small">Maiores Sucessos</h3>
            </div>
            <div class="hits-grid" id="hitsGrid">
                <!-- Hit songs will be loaded by JavaScript -->
            </div>
        </div>
    </section>

    <!-- Live Stats Section -->
    <section id="stats" class="stats">
        <div class="container">
            <div class="section-header">
                <h2 class="section-title">Estatísticas ao Vivo</h2>
                <p class="section-subtitle">
                    Dados em tempo real mostrando o impacto global contínuo do One Direction
                </p>
            </div>
            <div class="stats-grid" id="statsGrid">
                <div class="loading">Carregando estatísticas...</div>
            </div>
            <div class="stats-info" id="statsInfo"></div>
            <div class="api-credit">
                <p>Dados fornecidos pela API Last.fm • Atualizado em tempo real</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-brand">
                    <h3>One Direction</h3>
                    <p>Celebrando a incrível jornada do One Direction - a banda que trouxe alegria, música e memórias para milhões de fãs ao redor do mundo.</p>
                    <div class="social-links">
                        <div class="social-icon">📘</div>
                        <div class="social-icon">🐦</div>
                        <div class="social-icon">📸</div>
                        <div class="social-icon">🎵</div>
                    </div>
                </div>
                <div class="footer-links">
                    <h4>Links Rápidos</h4>
                    <ul>
                        <li>Música</li>
                        <li>Membros da Banda</li>
                        <li>Álbuns</li>
                        <li>Linha do Tempo</li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Legado</h4>
                    <ul>
                        <li>Carreiras Solo</li>
                        <li>Comunidade de Fãs</li>
                        <li>Memórias</li>
                        <li>Tributos</li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>© 2024 One Direction Fan Experience. Feito com ❤️ para Directioners em todo o mundo.</p>
                <p>Este é um site tributo feito por fãs celebrando o incrível legado do One Direction.</p>
            </div>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

:root {
    /* Color Palette */
    --primary: hsl(262, 80%, 65%);
    --primary-glow: hsl(262, 80%, 75%);
    --secondary: hsl(196, 90%, 65%);
    --secondary-glow: hsl(196, 90%, 75%);
    --secondary-foreground: hsl(220, 20%, 10%);
    
    /* Background Colors */
    --background: hsl(220, 25%, 8%);
    --foreground: hsl(220, 15%, 95%);
    --card: hsl(220, 20%, 12%);
    --card-foreground: hsl(220, 15%, 90%);
    --muted: hsl(220, 15%, 15%);
    --muted-foreground: hsl(220, 10%, 60%);
    --border: hsl(220, 15%, 20%);
    
    /* Gradients */
    --gradient-primary: linear-gradient(135deg, var(--primary), var(--primary-glow));
    --gradient-secondary: linear-gradient(135deg, var(--secondary), var(--secondary-glow));
    --card-gradient: linear-gradient(145deg, hsl(220, 20%, 12%), hsl(220, 18%, 10%));
    --hero-gradient: linear-gradient(135deg, rgba(139, 69, 19, 0.8), rgba(0, 0, 0, 0.9));
    
    /* Shadows */
    --shadow-glow: 0 0 40px hsla(262, 80%, 65%, 0.3);
    --shadow-elegant: 0 10px 30px -10px hsla(262, 80%, 65%, 0.2);
    
    /* Transitions */
    --transition-smooth: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    
    /* Typography */
    --font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

body {
    font-family: var(--font-family);
    background-color: var(--background);
    color: var(--foreground);
    line-height: 1.6;
    overflow-x: hidden;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.5rem;
}

/* Navigation */
.nav {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(23, 25, 35, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
    z-index: 1000;
    transition: var(--transition-smooth);
}

.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-brand h1 {
    background: var(--gradient-primary);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    font-size: 1.5rem;
    font-weight: 800;
}

.nav-links {
    display: flex;
    gap: 2rem;
}

.nav-link {
    color: var(--foreground);
    text-decoration: none;
    font-weight: 500;
    transition: var(--transition-smooth);
    position: relative;
}

.nav-link:hover {
    color: var(--primary);
}

.nav-link::after {
    content: '';
    position: absolute;
    width: 100%;
    height: 2px;
    bottom: -4px;
    left: 0;
    background: var(--primary);
    transform: scaleX(0);
    transition: var(--transition-smooth);
}

.nav-link:hover::after {
    transform: scaleX(1);
}

.mobile-menu-btn {
    display: none;
    flex-direction: column;
    background: none;
    border: none;
    cursor: pointer;
    padding: 0.5rem;
}

.mobile-menu-btn span {
    width: 25px;
    height: 3px;
    background: var(--foreground);
    margin: 3px 0;
    transition: var(--transition-smooth);
}

/* Hero Section */
.hero {
    position: relative;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
}

.hero-bg {
    position: absolute;
    inset: 0;
    background: url('src/assets/hero-bg.jpg') center/cover no-repeat;
}

.hero-bg::after {
    content: '';
    position: absolute;
    inset: 0;
    background: var(--hero-gradient);
}

.hero-content {
    position: relative;
    z-index: 10;
    text-align: center;
    padding: 0 1.5rem;
    max-width: 64rem;
}

.hero-title {
    font-size: clamp(3rem, 8vw, 6rem);
    font-weight: 800;
    margin-bottom: 1.5rem;
    background: var(--gradient-primary);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: float 6s ease-in-out infinite;
}

.hero-subtitle {
    font-size: clamp(1.2rem, 2.5vw, 1.5rem);
    color: rgba(255, 255, 255, 0.9);
    margin-bottom: 2rem;
    max-width: 32rem;
    margin-left: auto;
    margin-right: auto;
}

.hero-buttons {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: center;
}

@media (min-width: 640px) {
    .hero-buttons {
        flex-direction: row;
        justify-content: center;
    }
}

/* Buttons */
.btn {
    padding: 1rem 2rem;
    font-size: 1.125rem;
    font-weight: 600;
    border: none;
    border-radius: 0.5rem;
    cursor: pointer;
    transition: var(--transition-smooth);
    text-decoration: none;
    display: inline-block;
    text-align: center;
}

.btn-primary {
    background: var(--primary);
    color: white;
    box-shadow: var(--shadow-glow);
}

.btn-primary:hover {
    background: var(--primary-glow);
    transform: translateY(-2px);
}

.btn-outline {
    border: 2px solid var(--secondary);
    color: var(--secondary);
    background: transparent;
}

.btn-outline:hover {
    background: var(--secondary);
    color: var(--secondary-foreground);
}

/* Floating Elements */
.floating-elements {
    position: absolute;
    inset: 0;
    pointer-events: none;
}

.float-1, .float-2, .float-3, .float-4 {
    position: absolute;
    border-radius: 50%;
    animation: float 6s ease-in-out infinite;
}

.float-1 {
    top: 5rem;
    left: 2.5rem;
    width: 1rem;
    height: 1rem;
    background: var(--primary);
    opacity: 0.6;
}

.float-2 {
    top: 10rem;
    right: 5rem;
    width: 1.5rem;
    height: 1.5rem;
    background: var(--secondary);
    opacity: 0.4;
    animation-delay: 1s;
}

.float-3 {
    bottom: 8rem;
    left: 5rem;
    width: 0.75rem;
    height: 0.75rem;
    background: var(--primary-glow);
    opacity: 0.5;
    animation-delay: 2s;
}

.float-4 {
    bottom: 5rem;
    right: 8rem;
    width: 1.25rem;
    height: 1.25rem;
    background: var(--secondary-glow);
    opacity: 0.3;
    animation-delay: 0.5s;
}

/* Sections */
.section-header {
    text-align: center;
    margin-bottom: 4rem;
}

.section-title {
    font-size: clamp(2.5rem, 6vw, 4rem);
    font-weight: 800;
    margin-bottom: 1.5rem;
    background: var(--gradient-primary);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

.section-title-small {
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 800;
    margin-bottom: 1.5rem;
    background: var(--gradient-secondary);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

.section-subtitle {
    font-size: 1.25rem;
    color: var(--muted-foreground);
    max-width: 48rem;
    margin: 0 auto;
}

/* Members Section */
.members {
    padding: 5rem 0;
}

.members-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}

.member-card {
    background: var(--card-gradient);
    border: 1px solid var(--border);
    border-radius: 1rem;
    padding: 2rem;
    text-align: center;
    transition: var(--transition-smooth);
    transform-origin: center;
}

.member-card:hover {
    box-shadow: var(--shadow-glow);
    transform: scale(1.05);
}

.member-emoji {
    font-size: 4rem;
    margin-bottom: 1rem;
    display: block;
    transition: var(--transition-smooth);
}

.member-card:hover .member-emoji {
    animation: bounce 0.6s ease-in-out;
}

.member-name {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 0.5rem;
}

.member-role {
    color: var(--secondary);
    font-weight: 600;
    margin-bottom: 1rem;
}

.member-description {
    color: var(--muted-foreground);
    font-size: 0.875rem;
}

/* Music Section */
.music {
    padding: 5rem 0;
    background: rgba(255, 255, 255, 0.02);
}

.albums-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-bottom: 5rem;
}

.album-card {
    background: var(--card-gradient);
    border: 1px solid var(--border);
    border-radius: 1rem;
    overflow: hidden;
    transition: var(--transition-smooth);
}

.album-card:hover {
    box-shadow: var(--shadow-glow);
    transform: scale(1.05);
}

.album-color {
    height: 0.5rem;
}

.album-content {
    padding: 2rem;
}

.album-title {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 0.5rem;
    transition: var(--transition-smooth);
}

.album-card:hover .album-title {
    color: var(--primary-glow);
}

.album-year {
    background: var(--secondary);
    color: var(--secondary-foreground);
    padding: 0.25rem 0.75rem;
    border-radius: 1rem;
    font-size: 0.875rem;
    font-weight: 600;
    display: inline-block;
    margin-bottom: 1rem;
}

.album-description {
    color: var(--muted-foreground);
    margin-bottom: 1.5rem;
}

.album-tracks h4 {
    color: var(--secondary);
    font-weight: 600;
    margin-bottom: 0.5rem;
}

.track-item {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: var(--card-foreground);
    font-size: 0.875rem;
    margin-bottom: 0.25rem;
}

.track-dot {
    width: 0.25rem;
    height: 0.25rem;
    background: var(--primary);
    border-radius: 50%;
}

.hits-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
}

.hit-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 0.5rem;
    padding: 1.5rem;
    transition: var(--transition-smooth);
}

.hit-card:hover {
    background: rgba(255, 255, 255, 0.05);
    box-shadow: var(--shadow-elegant);
}

.hit-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.hit-info h4 {
    font-size: 1.125rem;
    font-weight: 700;
    color: var(--primary);
    margin-bottom: 0.25rem;
    transition: var(--transition-smooth);
}

.hit-card:hover .hit-info h4 {
    color: var(--primary-glow);
}

.hit-meta {
    color: var(--muted-foreground);
    font-size: 0.875rem;
}

.hit-emoji {
    font-size: 1.5rem;
    animation: pulse 2s ease-in-out infinite;
}

/* Stats Section */
.stats {
    padding: 5rem 0;
    background: rgba(255, 255, 255, 0.02);
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
}

.stat-card {
    background: var(--card-gradient);
    border: 1px solid var(--border);
    border-radius: 1rem;
    padding: 2rem;
    text-align: center;
    transition: var(--transition-smooth);
}

.stat-card:hover {
    box-shadow: var(--shadow-glow);
}

.stat-title {
    color: var(--primary);
    font-size: 1.125rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.stat-value {
    font-size: 2.5rem;
    font-weight: 800;
    color: var(--secondary);
    margin-bottom: 0.5rem;
}

.stat-label {
    color: var(--muted-foreground);
    font-size: 0.875rem;
}

.stats-info {
    background: var(--card-gradient);
    border: 1px solid var(--border);
    border-radius: 1rem;
    padding: 2rem;
    margin-bottom: 2rem;
}

.stats-info h3 {
    color: var(--primary);
    text-align: center;
    margin-bottom: 1rem;
    font-size: 1.5rem;
}

.stats-info p {
    color: var(--muted-foreground);
    text-align: center;
    max-width: 64rem;
    margin: 0 auto;
}

.api-credit {
    text-align: center;
}

.api-credit p {
    color: var(--muted-foreground);
    font-size: 0.75rem;
}

.loading {
    text-align: center;
    color: var(--muted-foreground);
    font-size: 1.125rem;
    padding: 2rem;
}

/* Footer */
.footer {
    background: rgba(255, 255, 255, 0.05);
    border-top: 1px solid var(--border);
    padding: 3rem 0;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-bottom: 2rem;
}

.footer-brand h3 {
    font-size: 1.5rem;
    font-weight: 800;
    margin-bottom: 1rem;
    background: var(--gradient-primary);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}

.footer-brand p {
    color: var(--muted-foreground);
    margin-bottom: 1rem;
    max-width: 24rem;
}

.social-links {
    display: flex;
    gap: 1rem;
}

.social-icon {
    width: 2rem;
    height: 2rem;
    background: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: var(--transition-smooth);
}

.social-icon:hover {
    background: rgba(255, 255, 255, 0.2);
}

.footer-links h4 {
    color: var(--primary);
    font-size: 1.125rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.footer-links ul {
    list-style: none;
}

.footer-links li {
    color: var(--muted-foreground);
    margin-bottom: 0.5rem;
    cursor: pointer;
    transition: var(--transition-smooth);
}

.footer-links li:hover {
    color: var(--foreground);
}

.footer-bottom {
    border-top: 1px solid var(--border);
    padding-top: 2rem;
    text-align: center;
}

.footer-bottom p {
    color: var(--muted-foreground);
    margin-bottom: 0.5rem;
}

/* Animations */
@keyframes float {
    0%, 100% {
        transform: translateY(0px);
    }
    50% {
        transform: translateY(-20px);
    }
}

@keyframes bounce {
    0%, 20%, 53%, 80%, 100% {
        animation-timing-function: cubic-bezier(0.215, 0.610, 0.355, 1.000);
        transform: translate3d(0, 0, 0);
    }
    40%, 43% {
        animation-timing-function: cubic-bezier(0.755, 0.050, 0.855, 0.060);
        transform: translate3d(0, -30px, 0);
    }
    70% {
        animation-timing-function: cubic-bezier(0.755, 0.050, 0.855, 0.060);
        transform: translate3d(0, -15px, 0);
    }
    90% {
        transform: translate3d(0, -4px, 0);
    }
}

@keyframes pulse {
    0%, 100% {
        opacity: 1;
    }
    50% {
        opacity: 0.5;
    }
}

/* Responsive Design */
@media (max-width: 768px) {
    .nav-links {
        display: none;
    }
    
    .mobile-menu-btn {
        display: flex;
    }
    
    .members-grid {
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    }
    
    .albums-grid {
        grid-template-columns: 1fr;
    }
    
    .hits-grid {
        grid-template-columns: 1fr;
    }
    
    .stats-grid {
        grid-template-columns: 1fr;
    }
    
    .footer-content {
        grid-template-columns: 1fr;
        text-align: center;
    }
}

// API Configuration
const API_KEY = '174b9ac26b0e4d613e8c5d8b1e4c5e8e'; // Last.fm API Key
const API_BASE_URL = 'https://ws.audioscrobble.com/2.0/';

// Data
const members = [
    {
        name: "Harry Styles",
        role: "Vocal Principal",
        description: "Conhecido por sua voz distintiva e presença carismática no palco",
        image: "🎤"
    },
    {
        name: "Niall Horan", 
        role: "Guitarra & Vocal",
        description: "Músico irlandês trazendo habilidades de guitarra e harmonias",
        image: "🎸"
    },
    {
        name: "Louis Tomlinson",
        role: "Vocal",
        description: "Vocal forte e contribuições para composição de músicas",
        image: "🎵"
    },
    {
        name: "Liam Payne",
        role: "Vocal",
        description: "Vocal versátil e habilidades de beatbox",
        image: "🎶"
    },
    {
        name: "Zayn Malik",
        role: "Vocal (2010-2015)",
        description: "Vocal agudo e influência R&B durante seu tempo com a banda",
        image: "⭐"
    }
];

const albums = [
    {
        title: "Up All Night",
        year: "2011",
        description: "Seu álbum de estreia que os lançou ao estrelato internacional",
        songs: ["What Makes You Beautiful", "Gotta Be You", "One Thing"],
        color: "linear-gradient(135deg, #3b82f6, #8b5cf6)"
    },
    {
        title: "Take Me Home", 
        year: "2012",
        description: "Segundo álbum de estúdio com um som mais maduro",
        songs: ["Live While We're Young", "Little Things", "Kiss You"],
        color: "linear-gradient(135deg, #8b5cf6, #ec4899)"
    },
    {
        title: "Midnight Memories",
        year: "2013", 
        description: "Terceiro álbum com influência rock mostrando sua evolução",
        songs: ["Best Song Ever", "Story of My Life", "Diana"],
        color: "linear-gradient(135deg, #6366f1, #3b82f6)"
    },
    {
        title: "Four",
        year: "2014",
        description: "Quarto álbum com composições mais profundas e temas",
        songs: ["Steal My Girl", "Night Changes", "18"],
        color: "linear-gradient(135deg, #14b8a6, #10b981)"
    },
    {
        title: "Made in the A.M.",
        year: "2015",
        description: "Álbum final como grupo, mostrando sua maturidade artística",
        songs: ["Drag Me Down", "Perfect", "History"],
        color: "linear-gradient(135deg, #f97316, #ef4444)"
    }
];

const hitSongs = [
    { title: "What Makes You Beautiful", album: "Up All Night", year: "2011" },
    { title: "Story of My Life", album: "Midnight Memories", year: "2013" },
    { title: "Best Song Ever", album: "Midnight Memories", year: "2013" },
    { title: "Night Changes", album: "Four", year: "2014" },
    { title: "Drag Me Down", album: "Made in the A.M.", year: "2015" },
    { title: "Perfect", album: "Made in the A.M.", year: "2015" }
];

// Utility Functions
function scrollToSection(sectionId) {
    const element = document.getElementById(sectionId);
    if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
    }
}

function formatNumber(num) {
    const number = parseInt(num);
    if (number >= 1000000000) {
        return (number / 1000000000).toFixed(1) + 'B';
    }
    if (number >= 1000000) {
        return (number / 1000000).toFixed(1) + 'M';
    }
    if (number >= 1000) {
        return (number / 1000).toFixed(1) + 'K';
    }
    return number.toString();
}

// DOM Manipulation Functions
function loadMembers() {
    const membersGrid = document.getElementById('membersGrid');
    
    members.forEach(member => {
        const memberCard = document.createElement('div');
        memberCard.className = 'member-card';
        memberCard.innerHTML = `
            <span class="member-emoji">${member.image}</span>
            <h3 class="member-name">${member.name}</h3>
            <p class="member-role">${member.role}</p>
            <p class="member-description">${member.description}</p>
        `;
        membersGrid.appendChild(memberCard);
    });
}

function loadAlbums() {
    const albumsGrid = document.getElementById('albumsGrid');
    
    albums.forEach(album => {
        const albumCard = document.createElement('div');
        albumCard.className = 'album-card';
        albumCard.innerHTML = `
            <div class="album-color" style="background: ${album.color}"></div>
            <div class="album-content">
                <h3 class="album-title">${album.title}</h3>
                <span class="album-year">${album.year}</span>
                <p class="album-description">${album.description}</p>
                <div class="album-tracks">
                    <h4>Faixas em Destaque:</h4>
                    ${album.songs.map(song => `
                        <div class="track-item">
                            <span class="track-dot"></span>
                            ${song}
                        </div>
                    `).join('')}
                </div>
            </div>
        `;
        albumsGrid.appendChild(albumCard);
    });
}

function loadHitSongs() {
    const hitsGrid = document.getElementById('hitsGrid');
    
    hitSongs.forEach(song => {
        const hitCard = document.createElement('div');
        hitCard.className = 'hit-card';
        hitCard.innerHTML = `
            <div class="hit-content">
                <div class="hit-info">
                    <h4>${song.title}</h4>
                    <p class="hit-meta">${song.album} • ${song.year}</p>
                </div>
                <div class="hit-emoji">🎵</div>
            </div>
        `;
        hitsGrid.appendChild(hitCard);
    });
}

// API Functions - Using Last.fm API
async function fetchArtistData() {
    const statsGrid = document.getElementById('statsGrid');
    const statsInfo = document.getElementById('statsInfo');
    
    try {
        const response = await fetch(
            `${API_BASE_URL}?method=artist.getinfo&artist=One Direction&api_key=${API_KEY}&format=json`
        );
        
        if (!response.ok) {
            throw new Error('Falha ao buscar dados da API');
        }
        
        const data = await response.json();
        
        if (data.artist) {
            displayStats(data.artist);
            displayArtistInfo(data.artist);
        } else {
            throw new Error('Dados do artista não encontrados');
        }
    } catch (error) {
        console.error('Erro ao buscar dados do artista:', error);
        displayFallbackStats();
    }
}

function displayStats(artistData) {
    const statsGrid = document.getElementById('statsGrid');
    
    statsGrid.innerHTML = `
        <div class="stat-card">
            <h3 class="stat-title">Total de Reproduções</h3>
            <div class="stat-value">${formatNumber(artistData.playcount || '0')}</div>
            <p class="stat-label">Em todas as plataformas</p>
        </div>
        <div class="stat-card">
            <h3 class="stat-title">Ouvintes Mensais</h3>
            <div class="stat-value">${formatNumber(artistData.listeners || '0')}</div>
            <p class="stat-label">Ouvintes ativos mensais</p>
        </div>
        <div class="stat-card">
            <h3 class="stat-title">Status do Legado</h3>
            <div class="stat-value">Ainda #1</div>
            <p class="stat-label">Em nossos corações ❤️</p>
        </div>
    `;
}

function displayArtistInfo(artistData) {
    const statsInfo = document.getElementById('statsInfo');
    
    if (artistData.bio && artistData.bio.summary) {
        const summary = artistData.bio.summary.replace(/<[^>]*>/g, '').split('.')[0] + '.';
        statsInfo.innerHTML = `
            <h3>Sobre o One Direction</h3>
            <p>${summary}</p>
        `;
    }
}

function displayFallbackStats() {
    const statsGrid = document.getElementById('statsGrid');
    const statsInfo = document.getElementById('statsInfo');
    
    // Dados de fallback caso a API falhe
    statsGrid.innerHTML = `
        <div class="stat-card">
            <h3 class="stat-title">Total de Reproduções</h3>
            <div class="stat-value">2.8B</div>
            <p class="stat-label">Em todas as plataformas</p>
        </div>
        <div class="stat-card">
            <h3 class="stat-title">Ouvintes Mensais</h3>
            <div class="stat-value">1.8M</div>
            <p class="stat-label">Ouvintes ativos mensais</p>
        </div>
        <div class="stat-card">
            <h3 class="stat-title">Status do Legado</h3>
            <div class="stat-value">Ainda #1</div>
            <p class="stat-label">Em nossos corações ❤️</p>
        </div>
    `;
    
    statsInfo.innerHTML = `
        <h3>Sobre o One Direction</h3>
        <p>One Direction foi uma boy band pop britânico-irlandesa formada em Londres, Inglaterra em 2010. O grupo é composto por Niall Horan, Liam Payne, Harry Styles e Louis Tomlinson.</p>
    `;
}

// Mobile Menu Toggle
function setupMobileMenu() {
    const mobileMenuBtn = document.getElementById('mobileMenuBtn');
    const navLinks = document.querySelector('.nav-links');
    
    mobileMenuBtn.addEventListener('click', () => {
        navLinks.classList.toggle('active');
    });
}

// Smooth Scrolling for Navigation Links
function setupSmoothScrolling() {
    const navLinks = document.querySelectorAll('.nav-link');
    
    navLinks.forEach(link => {
        link.addEventListener('click', (e) => {
            e.preventDefault();
            const targetId = link.getAttribute('href').substring(1);
            scrollToSection(targetId);
        });
    });
}

// Initialize App
function initApp() {
    // Load static content
    loadMembers();
    loadAlbums();
    loadHitSongs();
    
    // Fetch dynamic data from API
    fetchArtistData();
    
    // Setup interactivity
    setupMobileMenu();
    setupSmoothScrolling();
}

// Start the app when DOM is loaded
document.addEventListener('DOMContentLoaded', initApp);

// Add some extra CSS for mobile menu functionality
const mobileMenuStyles = `
    @media (max-width: 768px) {
        .nav-links.active {
            display: flex;
            position: absolute;
            top: 100%;
            left: 0;
            right: 0;
            background: rgba(23, 25, 35, 0.98);
            flex-direction: column;
            padding: 1rem;
            border-top: 1px solid var(--border);
        }
    }
`;

// Inject mobile menu styles
const styleSheet = document.createElement('style');
styleSheet.textContent = mobileMenuStyles;
document.head.appendChild(styleSheet);
