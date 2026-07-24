# Cours-d-arabe-pour-ma-Hbiba-Sarah
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apprendre l'Arabe - Niveau Débutant</title>
    <style>
        :root {
            --primary: #2c3e50;
            --accent: #e74c3c;
            --bg: #f8f9fa;
            --card-bg: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
        }

        /* Les bordures/extrémités avec le message personnalisé */
        .sidebar {
            position: fixed;
            top: 0;
            bottom: 0;
            width: 80px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: transparent;
            color: var(--accent);
            font-weight: bold;
            font-size: 1.2rem;
            text-align: center;
            z-index: 10;
            pointer-events: none; /* Évite de bloquer le clic */
        }

        .sidebar-left {
            left: 10px;
            writing-mode: vertical-rl;
            transform: rotate(180deg);
        }

        .sidebar-right {
            right: 10px;
            writing-mode: vertical-rl;
        }

        /* Conteneur principal */
        .container {
            max-width: 900px;
            width: 100%;
            margin: 0 100px; /* Laisse de la place pour les messages sur les côtés */
            padding: 40px 20px;
            box-sizing: border-box;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            color: var(--primary);
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        header p {
            color: #7f8c8d;
            font-size: 1.1rem;
        }

        /* Grille des lettres */
        .alphabet-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 20px;
        }

        /* Cartes des lettres */
        .letter-card {
            background-color: var(--card-bg);
            border-radius: 12px;
            padding: 25px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: transform 0.2s, box-shadow 0.2s;
            border: 1px solid #e2e8f0;
        }

        .letter-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0,0,0,0.1);
            border-color: var(--accent);
        }

        .arabic-letter {
            font-size: 3.5rem;
            color: var(--primary);
            margin: 0 0 10px 0;
            font-family: 'Amiri', 'Traditional Arabic', serif;
        }

        .letter-name {
            font-weight: bold;
            font-size: 1.2rem;
            color: #2d3748;
            margin-bottom: 5px;
        }

        .letter-pronunciation {
            color: #718096;
            font-size: 0.95rem;
            font-style: italic;
        }

        /* Zone d'affichage des détails quand on clique */
        .info-box {
            background-color: #ebf8ff;
            border-left: 4px solid #3182ce;
            padding: 15px;
            margin-bottom: 30px;
            border-radius: 0 8px 8px 0;
            text-align: center;
            font-size: 1.1rem;
            display: none;
        }

        /* Responsive basique */
        @media (max-width: 600px) {
            .container { margin: 0 50px; }
            .sidebar { font-size: 0.9rem; width: 40px; }
        }
    </style>
</head>
<body>

    <!-- Extrémités avec le message d'amour -->
    <div class="sidebar sidebar-left">❤️ Je t'aime Sarah ❤️</div>
    <div class="sidebar sidebar-right">❤️ Je t'aime Sarah ❤️</div>

    <!-- Contenu Principal de l'apprentissage -->
    <div class="container">
        <header>
            <h1>Apprendre l'Alphabet Arabe</h1>
            <p>Niveau Débutant — Cliquez sur une lettre pour vous entraîner !</p>
        </header>

        <div id="infoBox" class="info-box"></div>

        <div class="alphabet-grid">
            <!-- Lettre 1 -->
            <div class="letter-card" onclick="showInfo('Alif', 'Se prononce comme le \'a\' dans \'papa\'. C\'est une extension de son.')">
                <div class="arabic-letter">أ</div>
                <div class="letter-name">Alif</div>
                <div class="letter-pronunciation">Son : [a]</div>
            </div>

            <!-- Lettre 2 -->
            <div class="letter-card" onclick="showInfo('Ba', 'Se prononce exactement comme le \'b\' français.')">
                <div class="arabic-letter">ب</div>
                <div class="letter-name">Ba</div>
                <div class="letter-pronunciation">Son : [b]</div>
            </div>

            <!-- Lettre 3 -->
            <div class="letter-card" onclick="showInfo('Ta', 'Se prononce comme le \'t\' français, avec le bout de la langue sur les dents.')">
                <div class="arabic-letter">ت</div>
                <div class="letter-name">Ta</div>
                <div class="letter-pronunciation">Son : [t]</div>
            </div>

            <!-- Lettre 4 -->
            <div class="letter-card" onclick="showInfo('Tha', 'Se prononce comme le \'th\' anglais dans \'think\'. On place la langue sous les dents de devant.')">
                <div class="arabic-letter">ث</div>
                <div class="letter-name">Tha</div>
                <div class="letter-pronunciation">Son : [th]</div>
            </div>

            <!-- Lettre 5 -->
            <div class="letter-card" onclick="showInfo('Jeem', 'Se prononce comme le \'j\' en anglais (comme dans \'John\') ou le \'dj\' en français.')">
                <div class="arabic-letter">ج</div>
                <div class="letter-name">Jeem</div>
                <div class="letter-pronunciation">Son : [dj]</div>
            </div>

            <!-- Lettre 6 -->
            <div class="letter-card" onclick="showInfo('Ha', 'Un \'h\' très expiré qui vient du fond de la gorge, comme si on voulait faire de la buée sur une vitre.')">
                <div class="arabic-letter">ح</div>
                <div class="letter-name">Ha</div>
                <div class="letter-pronunciation">Son : [h expiré]</div>
            </div>

            <!-- Lettre 7 -->
            <div class="letter-card" onclick="showInfo('Kha', 'Un son raclé, similaire au \'j\' espagnol (jota) ou au \'ch\' allemand dans \'Bach\'.')">
                <div class="arabic-letter">خ</div>
                <div class="letter-name">Kha</div>
                <div class="letter-pronunciation">Son : [kh raclé]</div>
            </div>

            <!-- Lettre 8 -->
            <div class="letter-card" onclick="showInfo('Dal', 'Se prononce comme le \'d\' français.')">
                <div class="arabic-letter">د</div>
                <div class="letter-name">Dal</div>
                <div class="letter-pronunciation">Son : [d]</div>
            </div>
        </div>
    </div>

    <script>
        // Petite fonction interactive pour afficher des conseils de prononciation au clic
        function showInfo(name, description) {
            const infoBox = document.getElementById('infoBox');
            infoBox.style.display = 'block';
            infoBox.innerHTML = `<strong>${name}</strong> : ${description}`;
        }
    </script>
</body>
</html>
