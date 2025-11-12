<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cours et Exercices Corrigés – Mécanique Rationnelle</title>
<style>
    body { font-family: Arial, sans-serif; margin:0; padding:0; background:#f5f5f5; }
    header { background:#004080; color:white; padding:20px; text-align:center; }
    nav { background:#0066cc; padding:10px; }
    nav a { color:white; margin:0 15px; text-decoration:none; font-weight:bold; }
    nav a:hover { text-decoration:underline; }
    .container { padding:20px; max-width:1000px; margin:auto; background:white; }
    .lang { display:none; }
    h1, h2, h3 { color:#004080; }
    select { margin-left:10px; padding:5px; }
    footer { background:#004080; color:white; text-align:center; padding:10px; margin-top:20px; }
    pre { background:#eee; padding:10px; overflow-x:auto; }
</style>
</head>
<body>

<header>
    <h1 id="title">Cours et Exercices Corrigés – Mécanique Rationnelle</h1>
    <label for="language">Choisir la langue :</label>
    <select id="language" onchange="changeLanguage()">
        <option value="fr">Français</option>
        <option value="en">English</option>
    </select>
</header>

<nav>
    <a href="#cours" class="lang fr">Cours</a>
    <a href="#exercices" class="lang fr">Exercices</a>
    <a href="#solutions" class="lang fr">Solutions</a>

    <a href="#cours" class="lang en">Course</a>
    <a href="#exercices" class="lang en">Exercises</a>
    <a href="#solutions" class="lang en">Solutions</a>
</nav>

<div class="container">

    <!-- Section Cours -->
    <section id="cours">
        <h2 class="lang fr">Cours – Mécanique Rationnelle</h2>
        <h2 class="lang en">Course – Rational Mechanics</h2>
        <p class="lang fr">
            Ce cours couvre les principes fondamentaux de la mécanique rationnelle, incluant le calcul des torseurs, vecteurs glissants, moments et cinématique des solides.
        </p>
        <p class="lang en">
            This course covers the fundamental principles of rational mechanics, including the calculation of torsors, sliding vectors, moments, and solid kinematics.
        </p>
    </section>

    <!-- Section Exercices -->
    <section id="exercices">
        <h2 class="lang fr">Exercices</h2>
        <h2 class="lang en">Exercises</h2>

        <article>
            <h3 class="lang fr">Exercice 01</h3>
            <h3 class="lang en">Exercise 01</h3>
            <p class="lang fr">
                Dans un repère orthonormé Oxyz, deux points A(2,2,-3) et B(5,3,2) sont donnés. Déterminer le moment du vecteur glissant AB par rapport au point O et par rapport à la droite Δ passant par O et C(2,2,1).
            </p>
            <p class="lang en">
                In an orthonormal coordinate system Oxyz, two points A(2,2,-3) and B(5,3,2) are given. Determine the moment of the sliding vector AB relative to point O and relative to the line Δ passing through O and C(2,2,1).
            </p>
        </article>

        <article>
            <h3 class="lang fr">Exercice 02</h3>
            <h3 class="lang en">Exercise 02</h3>
            <p class="lang fr">
                Ajouter ici un autre exercice...
            </p>
            <p class="lang en">
                Add another exercise here...
            </p>
        </article>

    </section>

    <!-- Section Solutions -->
    <section id="solutions">
        <h2 class="lang fr">Solutions</h2>
        <h2 class="lang en">Solutions</h2>

        <article>
            <h3 class="lang fr">Solution Exercice 01</h3>
            <h3 class="lang en">Solution Exercise 01</h3>
            <pre class="lang fr">
Vecteurs :
AB = B - A = (3,1,5)
OA = A - O = (2,2,-3)

Moment par rapport à O :
M_O = OA ∧ AB = 13i - 19j - 4k

Moment par rapport à la droite Δ (O→C) :
OC = (2,2,1), u = OC / |OC| = (2/3, 2/3, 1/3)
M_Δ = M_O - (M_O • u) u = (149/9)i - (139/9)j - (20/9)k
            </pre>
            <pre class="lang en">
Vectors:
AB = B - A = (3,1,5)
OA = A - O = (2,2,-3)

Moment relative to O:
M_O = OA ∧ AB = 13i - 19j - 4k

Moment relative to line Δ (O→C):
OC = (2,2,1), u = OC / |OC| = (2/3, 2/3, 1/3)
M_Δ = M_O - (M_O • u) u = (149/9)i - (139/9)j - (20/9)k
            </pre>
        </article>

    </section>

</div>

<footer>
    <p class="lang fr">© 2025 A. KADI – UMBB Boumerdès, Département de Physique</p>
    <p class="lang en">© 2025 A. KADI – UMBB Boumerdès, Department of Physics</p>
</footer>

<script>
function changeLanguage() {
    const lang = document.getElementById('language').value;
    document.querySelectorAll('.lang').forEach(el => {
        el.style.display = el.classList.contains(lang) ? 'block' : 'none';
    });
}
// Initialisation par défaut
changeLanguage();
</script>

</body>
</html>
