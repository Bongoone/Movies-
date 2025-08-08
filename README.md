
<html lang="sw">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movies 10 - Filamu 10 Bora za 2025</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #e50914;
            --dark: #141414;
            --light: #f4f4f4;
            --gray: #999;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: var(--dark);
            color: var(--light);
        }
        
        .header {
            padding: 20px 50px;
            position: relative;
            z-index: 10;
            background: linear-gradient(to bottom, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0) 100%);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            color: var(--primary);
            font-size: 2.5rem;
            font-weight: bold;
            text-decoration: none;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .nav-links {
            display: flex;
            gap: 20px;
        }
        
        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .hero {
            position: relative;
            height: 80vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://via.placeholder.com/1920x1080') center/cover no-repeat;
            display: flex;
            flex-direction: column;
            justify-content: center;
            padding: 0 50px;
        }
        
        .hero-content {
            max-width: 600px;
            z-index: 2;
        }
        
        .hero-title {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, #e50914, #f5f5f1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: slideIn 1s ease-out;
        }
        
        @keyframes slideIn {
            from { transform: translateX(-50px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        .hero-desc {
            font-size: 1.2rem;
            margin-bottom: 30px;
            line-height: 1.6;
            animation: fadeIn 1.5s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .download-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2rem;
            border-radius: 5px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
            40% {transform: translateY(-20px);}
            60% {transform: translateY(-10px);}
        }
        
        .download-btn:hover {
            background-color: #f40612;
            transform: scale(1.05);
        }
        
        .download-btn::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: rgba(255,255,255,0.1);
            transform: rotate(45deg);
            transition: all 0.3s;
        }
        
        .download-btn:hover::after {
            left: 100%;
        }
        
        .movies-section {
            padding: 50px;
        }
        
        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .section-title::after {
            content: '';
            flex: 1;
            height: 3px;
            background: linear-gradient(to right, var(--primary), transparent);
        }
        
        .movies-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .movie-card {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
            cursor: pointer;
        }
        
        .movie-card:hover {
            transform: scale(1.05);
            z-index: 1;
        }
        
        .movie-poster {
            width: 100%;
            height: 350px;
            object-fit: cover;
            display: block;
        }
        
        .movie-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.9), transparent);
            padding: 20px;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .movie-card:hover .movie-overlay {
            opacity: 1;
        }
        
        .movie-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: white;
        }
        
        .movie-desc {
            font-size: 0.9rem;
            color: var(--gray);
            margin-bottom: 15px;
            line-height: 1.4;
        }
        
        .movie-rating {
            display: flex;
            align-items: center;
            gap: 5px;
            color: gold;
            margin-bottom: 15px;
        }
        
        .card-download-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 5px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.9rem;
            transition: background-color 0.3s;
            width: 100%;
            justify-content: center;
        }
        
        .card-download-btn:hover {
            background-color: #f40612;
        }
        
        .floating-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: var(--primary);
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            z-index: 100;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        .floating-btn:hover {
            animation: none;
            transform: scale(1.1);
        }
        
        .footer {
            background-color: #000;
            padding: 50px;
            text-align: center;
            margin-top: 50px;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .footer-links a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--primary);
        }
        
        .copyright {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .marquee {
            background-color: rgba(229, 9, 20, 0.2);
            padding: 15px 0;
            overflow: hidden;
            white-space: nowrap;
            margin-bottom: 30px;
        }
        
        .marquee-content {
            display: inline-block;
            animation: marquee 20s linear infinite;
            font-size: 1.2rem;
            color: var(--primary);
            font-weight: bold;
        }
        
        @keyframes marquee {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background-color: var(--dark);
            padding: 30px;
            border-radius: 10px;
            max-width: 600px;
            width: 90%;
            position: relative;
            border: 2px solid var(--primary);
            animation: modalFadeIn 0.5s;
        }
        
        @keyframes modalFadeIn {
            from { opacity: 0; transform: scale(0.8); }
            to { opacity: 1; transform: scale(1); }
        }
        
        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            color: var(--gray);
            cursor: pointer;
            transition: color 0.3s;
        }
        
        .close-modal:hover {
            color: var(--primary);
        }
        
        .modal-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .modal-desc {
            margin-bottom: 30px;
            line-height: 1.6;
        }
        
        .modal-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            margin: 0 auto;
            transition: background-color 0.3s;
        }
        
        .modal-btn:hover {
            background-color: #f40612;
        }
        
        .highlight-text {
            background: linear-gradient(to right, #e50914, #f5f5f1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-weight: bold;
            animation: colorChange 3s infinite alternate;
        }
        
        @keyframes colorChange {
            0% { filter: hue-rotate(0deg); }
            100% { filter: hue-rotate(360deg); }
        }
    </style>
</head>
<body>
    <div class="header">
        <a href="#" class="logo">MOVIES </a>
      
    </div>
    
    <div class="marquee">
        <div class="marquee-content">
            🎬 FILAMU 10 BORA ZA MWAKA 2025 • KILA MTU ANAHITAJI KUTAZAMA HIZI FILAMU • BONYEZA KUPakua SASA • 🎬 FILAMU 10 BORA ZA MWAKA 2025 • KILA MTU ANAHITAJI KUTAZAMA HIZI FILAMU • BONYEZA KUPakua SASA •
        </div>
    </div>
    
    <section class="hero">
        <div class="hero-content">
            <h1 class="hero-title">Filamu 10 Bora za 2025</h1>
            <p class="hero-desc">
                <span class="highlight-text">Kumbukumbu ya kwanza!</span> Pakua filamu 10 bora za mwaka 2025 kwa ubora wa hali ya juu. 
                Utaona filamu zilizo na hadithi nzuri, uigizaji bora na matukio ya kusisimua ambayo hayataweza kukosa kukuvutia.
            </p>
            <button class="download-btn" onclick="showDownloadModal()">
                <i class="fas fa-download"></i> Pakua Sasa
            </button>
        </div>
    </section>
    
    <section class="movies-section">
        <h2 class="section-title">
            <i class="fas fa-trophy"></i> Filamu Bora za 2025
        </h2>
        <div class="movies-grid">
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/wtah7l.jpeg" alt="Movie 1" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Mwisho wa Safari</h3>
                    <p class="movie-desc">Hadithi ya kusisimua ya wanyama porini na mazingira magumu yanayowakabili.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.5/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/bxrnhy.jpeg" alt="Movie 2" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Mfalme wa Simba</h3>
                    <p class="movie-desc">Simba anarudi katika safari mpya ya kuvutia na matukio ya kushangaza.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.3/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/egz0ab.jpeg" alt="Movie 3" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Wakanda Milele</h3>
                    <p class="movie-desc">Wakanda inakabiliwa na hatari mpya inayodai ujasiri wa Black Panther mpya.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.7/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/uu362i.jpeg" alt="Movie 4" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Mstari wa Mwisho</h3>
                    <p class="movie-desc">Timu ya maandamano inakabiliana na majaribio ya kuua kila mwanachama wake.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.1/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/993n6q.jpeg" alt="Movie 5" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Macho ya Jini</h3>
                    <p class="movie-desc">Kijana anayegundua uwezo wa kuona mambo ya ajabu na kujikuta katika hatari.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>8.9/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/pcb8kl.jpeg" alt="Movie 6" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Mvua ya Mawe</h3>
                    <p class="movie-desc">Dunia inakabiliwa na mabadiliko ya hali ya hewa yenye kutisha na kusisimua.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.0/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/mtikxd.jpeg" alt="Movie 7" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Siri ya Fahali</h3>
                    <p class="movie-desc">Fahali anayefichua siri za kihistoria za ukoo wake na kujikuta katika hatari.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>8.8/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/xp4yqp.jpeg" alt="Movie 8" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Mchezo wa Mwisho</h3>
                    <p class="movie-desc">Wachezaji wa mchezo wa kuigiza wanajifunza kwamba mchezo wao sio wa kuigiza tu.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.2/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/3quept.jpeg" alt="Movie 9" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Nchi ya Ajabu</h3>
                    <p class="movie-desc">Watoto wawili wanaingia kwenye ulimwengu wa kufurahisha na wa hatari.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>8.7/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
            
            <div class="movie-card" onclick="showDownloadModal()">
                <img src="https://files.catbox.moe/fxd624.jpeg" alt="Movie 10" class="movie-poster">
                <div class="movie-overlay">
                    <h3 class="movie-title">Kivuli cha Usiku</h3>
                    <p class="movie-desc">Mtu anayegundua uwezo wake wa kuwa kivuli na kutumia uwezo huo kwa madhumuni mazuri.</p>
                    <div class="movie-rating">
                        <i class="fas fa-star"></i>
                        <span>9.4/10</span>
                    </div>
                    <button class="card-download-btn">
                        <i class="fas fa-download"></i> Pakua Sasa
                    </button>
                </div>
            </div>
        </div>
    </section>
    
    <div class="floating-btn" onclick="showDownloadModal()">
        <i class="fas fa-download"></i>
    </div>
    
    <div class="footer">
        <div class="footer-links">
            <a href="#">Mawasiliano</a>
            <a href="#">Sheria na Masharti</a>
            <a href="#">Sera ya Faragha</a>
            <a href="#">Maswali Yanayoulizwa Mara kwa Mara</a>
        </div>
        <p class="copyright">© 2025 Movies 10. Haki zote zimehifadhiwa.</p>
    </div>
    
    <div class="modal" id="downloadModal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal()">&times;</span>
            <h2 class="modal-title">Pakua Filamu Bora za 2025!</h2>
            <p class="modal-desc">
                Karibu kwenye Movies 10! Bonyeza kitufe cha <span class="highlight-text">"Pakua Sasa"</span> chini 
                kupata filamu 10 bora za mwaka 2025 kwa ubora wa hali ya juu. Utafurahia filamu zilizo na hadithi nzuri, 
                uigizaji bora na matukio ya kusisimua ambayo hayataweza kukosa kukuvutia.
            </p>
            <button class="modal-btn" onclick="redirectToDownload()">
                <i class="fas fa-download"></i> Pakua Sasa
            </button>
        </div>
    </div>
    
    <script>
        function showDownloadModal() {
            document.getElementById('downloadModal').style.display = 'flex';
        }
        
        function closeModal() {
            document.getElementById('downloadModal').style.display = 'none';
        }
        
        function redirectToDownload() {
            window.location.href = 'https://otieu.com/4/8928219';
        }
        
        // Close modal when clicking outside of it
        window.onclick = function(event) {
            const modal = document.getElementById('downloadModal');
            if (event.target == modal) {
                closeModal();
            }
        }
        
        // Make all movie cards clickable to show download modal
        document.querySelectorAll('.movie-card').forEach(card => {
            card.addEventListener('click', showDownloadModal);
        });
    </script>
</body>
</html>
