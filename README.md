# Cours-d-arabe-pour-ma-Hbiba-Sarah
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apprendre l'Arabe - L'Alphabet Complet</title>
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
            font-size: 1.3rem;
            text-align: center;
            z-index: 10;
            pointer-events: none;
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
            max-width: 1000px;
            width: 100%;
            margin: 0 100px;
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

        /* Grille des lettres configurée pour la lecture de droite à gauche */
        .alphabet-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 20px;
            direction: rtl; /* Permet d'ordonner les cartes de droite à gauche */
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
            direction: ltr; /* Remet le texte explicatif en lecture normale gauche-droite */
            cursor: pointer;
        }

        .letter-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0,0,0,0.1);
            border-color: var(--accent);
        }

        .arabic-letter {
            font-size: 3.8rem;
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
            border-radius: 8px;
            text-align: center;
            font-size: 1.1rem;
            display: none;
        }

        @media (max-width: 768px) {
            .container { margin: 0 50px; }
            .sidebar { font-size: 1rem; width: 40px; }
        }
    </style>
</head>
<body>

    <!-- Extrémités avec le message d'amour -->
    <div class="sidebar sidebar-left">❤️ Je t'aime Sarah ❤️</div>
    <div class="sidebar sidebar-right">❤️ Je t'aime Sarah ❤️</div>

    <!-- Contenu Principal -->
    <div class="container">
        <header>
            <h1>L'Alphabet Arabe Complet</h1>
            <p>Cliquez sur une lettre pour découvrir son guide de prononciation détaillé.</p>
        </header>

        <div id="infoBox" class="info-box"></div>

        <div class="alphabet-grid">
            
            <!-- 1. Alif -->
            <div class="letter-card" onclick="showInfo('Alif (أ)', 'Sert de support au son \'a\' (comme dans papa) ou prolonge le son.')">
                <div class="arabic-letter">أ</div>
                <div class="letter-name">Alif</div>
                <div class="letter-pronunciation">[a]</div>
            </div>

            <!-- 2. Ba -->
            <div class="letter-card" onclick="showInfo('Ba (ب)', 'Se prononce exactement comme le \'b\' français.')">
                <div class="arabic-letter">ب</div>
                <div class="letter-name">Ba</div>
                <div class="letter-pronunciation">[b]</div>
            </div>

            <!-- 3. Ta -->
            <div class="letter-card" onclick="showInfo('Ta (ت)', 'Se prononce comme le \'t\' français.')">
                <div class="arabic-letter">ت</div>
                <div class="letter-name">Ta</div>
                <div class="letter-pronunciation">[t]</div>
            </div>

            <!-- 4. Tha -->
            <div class="letter-card" onclick="showInfo('Tha (ث)', 'Se prononce comme le \'th\' anglais dans \'think\'. Mettez la langue sous les dents du haut.')">
                <div class="arabic-letter">ث</div>
                <div class="letter-name">Tha</div>
                <div class="letter-pronunciation">[th]</div>
            </div>

            <!-- 5. Jeem -->
            <div class="letter-card" onclick="showInfo('Jeem (ج)', 'Se prononce comme le \'j\' anglais (comme dans John) ou \'dj\' en français.')">
                <div class="arabic-letter">ج</div>
                <div class="letter-name">Jeem</div>
                <div class="letter-pronunciation">[dj]</div>
            </div>

            <!-- 6. Ha -->
            <div class="letter-card" onclick="showInfo('Ha (ح)', 'Un \'h\' fortement expiré venant du milieu de la gorge (comme pour faire de la buée).')">
                <div class="arabic-letter">ح</div>
                <div class="letter-name">Ha</div>
                <div class="letter-pronunciation">[h expiré]</div>
            </div>

            <!-- 7. Kha -->
            <div class="letter-card" onclick="showInfo('Kha (خ)', 'Un son raclé, comme la \'jota\' espagnole ou le \'ch\' allemand dans Bach.')">
                <div class="arabic-letter">خ</div>
                <div class="letter-name">Kha</div>
                <div class="letter-pronunciation">[kh raclé]</div>
            </div>

            <!-- 8. Dal -->
            <div class="letter-card" onclick="showInfo('Dal (د)', 'Se prononce comme le \'d\' français.')">
                <div class="arabic-letter">د</div>
                <div class="letter-name">Dal</div>
                <div class="letter-pronunciation">[d]</div>
            </div>

            <!-- 9. Dhal -->
            <div class="letter-card" onclick="showInfo('Dhal (ذ)', 'Se prononce comme le \'th\' anglais dans \'this\'. Une version douce du \'d\'.')">
                <div class="arabic-letter">ذ</div>
                <div class="letter-name">Dhal</div>
                <div class="letter-pronunciation">[dh]</div>
            </div>

            <!-- 10. Ra -->
            <div class="letter-card" onclick="showInfo('Ra (ر)', 'Un \'r\' roulé avec le bout de la langue, comme en espagnol ou en italien.')">
                <div class="arabic-letter">ر</div>
                <div class="letter-name">Ra</div>
                <div class="letter-pronunciation">[r roulé]</div>
            </div>

            <!-- 11. Zay -->
            <div class="letter-card" onclick="showInfo('Zay (ز)', 'Se prononce comme le \'z\' français (comme dans zèbre).')">
                <div class="arabic-letter">ز</div>
                <div class="letter-name">Zay</div>
                <div class="letter-pronunciation">[z]</div>
            </div>

            <!-- 12. Seen -->
            <div class="letter-card" onclick="showInfo('Seen (س)', 'Se prononce comme le \'s\' français (comme dans sac).')">
                <div class="arabic-letter">س</div>
                <div class="letter-name">Seen</div>
                <div class="letter-pronunciation">[s]</div>
            </div>

            <!-- 13. Sheen -->
            <div class="letter-card" onclick="showInfo('Sheen (ش)', 'Se prononce comme le \'ch\' français (comme dans chat).')">
                <div class="arabic-letter">ش</div>
                <div class="letter-name">Sheen</div>
                <div class="letter-pronunciation">[ch]</div>
            </div>

            <!-- 14. Sad -->
            <div class="letter-card" onclick="showInfo('Sad (ص)', 'Un \'s\' emphatique, lourd et grave. On remplit la bouche en le prononçant.')">
                <div class="arabic-letter">ص</div>
                <div class="letter-name">Sad</div>
                <div class="letter-pronunciation">[s emphatique]</div>
            </div>

            <!-- 15. Dad -->
            <div class="letter-card" onclick="showInfo('Dad (ض)', 'Un \'d\' emphatique et très lourd. Le côté de la langue appuie contre les molaires.')">
                <div class="arabic-letter">ض</div>
                <div class="letter-name">Dad</div>
                <div class="letter-pronunciation">[d emphatique]</div>
            </div>

            <!-- 16. Ta (Emphatique) -->
            <div class="letter-card" onclick="showInfo('Ta (ط)', 'Un \'t\' emphatique et lourd, plus puissant que le \'Ta\' normal.')">
                <div class="arabic-letter">ط</div>
                <div class="letter-name">Ta (emp.)</div>
                <div class="letter-pronunciation">[t emphatique]</div>
            </div>

            <!-- 17. Dha (Emphatique) -->
            <div class="letter-card" onclick="showInfo('Dha (ظ)', 'Un \'dh\' emphatique, lourd et prononcé la langue contre les dents du haut.')">
                <div class="arabic-letter">ظ</div>
                <div class="letter-name">Dha (emp.)</div>
                <div class="letter-pronunciation">[dh emphatique]</div>
            </div>

            <!-- 18. Ayn -->
            <div class="letter-card" onclick="showInfo('Ayn (ع)', 'Un son typique produit par la contraction du fond de la gorge. Très particulier à l\'arabe !')">
                <div class="arabic-letter">ع</div>
                <div class="letter-name">Ayn</div>
                <div class="letter-pronunciation">[gorge]</div>
            </div>

            <!-- 19. Ghayn -->
            <div class="letter-card" onclick="showInfo('Ghayn (غ)', 'Proche du \'r\' français standard (comme dans Paris) ou d\'un gargarisme léger.')">
                <div class="arabic-letter">غ</div>
                <div class="letter-name">Ghayn</div>
                <div class="letter-pronunciation">[r français]</div>
            </div>

            <!-- 20. Fa -->
            <div class="letter-card" onclick="showInfo('Fa (ف)', 'Se prononce comme le \'f\' français.')">
                <div class="arabic-letter">ف</div>
                <div class="letter-name">Fa</div>
                <div class="letter-pronunciation">[f]</div>
            </div>

            <!-- 21. Qaf -->
            <div class="letter-card" onclick="showInfo('Qaf (ق)', 'Un \'k\' très profond, produit tout au fond de la gorge.')">
                <div class="arabic-letter">ق</div>
                <div class="letter-name">Qaf</div>
                <div class="letter-pronunciation">[k profond]</div>
            </div>

            <!-- 22. Kaf -->
            <div class="letter-card" onclick="showInfo('Kaf (ك)', 'Se prononce exactement comme le \'k\' ou \'c\' dur en français (comme dans kangourou).')">
                <div class="arabic-letter">ك</div>
                <div class="letter-name">Kaf</div>
                <div class="letter-pronunciation">[k]</div>
            </div>

            <!-- 23. Lam -->
            <div class="letter-card" onclick="showInfo('Lam (ل)', 'Se prononce comme le \'l\' français.')">
                <div class="arabic-letter">ل</div>
                <div class="letter-name">Lam</div>
                <div class="letter-pronunciation">[l]</div>
            </div>

            <!-- 24. Meem -->
            <div class="letter-card" onclick="showInfo('Meem (م)', 'Se prononce comme le \'m\' français.')">
                <div class="arabic-letter">م</div>
                <div class="letter-name">Meem</div>
                <div class="letter-pronunciation">[m]</div>
            </div>

            <!-- 25. Noon -->
            <div class="letter-card" onclick="showInfo('Noon (ن)', 'Se prononce comme le \'n\' français.')">
                <div class="arabic-letter">ن</div>
                <div class="letter-name">Noon</div>
                <div class="letter-pronunciation">[n]</div>
            </div>

            <!-- 26. Ha (Doux) -->
            <div class="letter-card" onclick="showInfo('Ha (هـ)', 'Un \'h\' aspiré et très doux, comme le \'h\' anglais dans \'hello\' ou \'home\'.')">
                <div class="arabic-letter">هـ</div>
                <div class="letter-name">Ha (doux)</div>
                <div class="letter-pronunciation">[h aspiré]</div>
            </div>

            <!-- 27. Waw -->
            <div class="letter-card" onclick="showInfo('Waw (و)', 'Se prononce comme le \'w\' dans \'web\' ou le \'ou\' dans \'oui\'.')">
                <div class="arabic-letter">و</div>
                <div class="letter-name">Waw</div>
                <div class="letter-pronunciation">[w] / [ou]</div>
            </div>

            <!-- 28. Ya -->
            <div class="letter-card" onclick="showInfo('Ya (ي)', 'Se prononce comme le \'y\' dans \'yoyo\' ou le \'i\' dans \'italie\'.')">
                <div class="arabic-letter">ي</div>
                <div class="letter-name">Ya</div>
                <div class="letter-pronunciation">[y] / [i]</div>
            </div>

        </div>
    </div>

    <script>
        function showInfo(name, description) {
            const infoBox = document.getElementById('infoBox');
            infoBox.style.display = 'block';
            infoBox.innerHTML = `<strong>${name}</strong> : ${description}`;
            // Fait défiler la page automatiquement vers l'explication si on est sur mobile
            infoBox.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
    </script>
</body>
</html>
