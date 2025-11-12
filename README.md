# Serie-TD-02Boumerdès – 
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Exercice Mécanique Rationnelle</title>
<style>
    body { font-family: Arial, sans-serif; margin: 20px; }
    .lang { display: none; }
</style>
</head>
<body>

<h1 id="title">UMBB Boumerdès – Faculté des Sciences</h1>

<label for="language">Choisir la langue :</label>
<select id="language" onchange="changeLanguage()">
    <option value="fr">Français</option>
    <option value="en">English</option>
</select>

<div class="content">

    <p class="lang fr">
        <strong>Département de Physique</strong><br>
        Cours : Mécanique Rationnelle – TCT et LMD-ST, Semestre 3
    </p>
    <p class="lang en">
        <strong>Department of Physics</strong><br>
        Course: Rational Mechanics – TCT and LMD-ST, Semester 3
    </p>

    <h2 class="lang fr">Exercice 01</h2>
    <h2 class="lang en">Exercise 01</h2>

    <p class="lang fr">
        Dans un repère orthonormé Oxyz, deux points A(2,2,-3) et B(5,3,2) sont donnés. <br>
        Déterminer le moment du vecteur glissant AB par rapport au point O et par rapport à la droite Δ passant par O et C(2,2,1).
    </p>

    <p class="lang en">
        In an orthonormal coordinate system Oxyz, two points A(2,2,-3) and B(5,3,2) are given. <br>
        Determine the moment of the sliding vector AB relative to point O and relative to the line Δ passing through O and C(2,2,1).
    </p>

</div>

<script>
function changeLanguage() {
    const lang = document.getElementById('language').value;
    document.querySelectorAll('.lang').forEach(el => {
        el.style.display = el.classList.contains(lang) ? 'block' : 'none';
    });
}

// Initialisation par défaut (français)
changeLanguage();
</script>

</body>
</html>
