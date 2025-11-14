from sympy import symbols, Matrix, simplify

# Définition des variables
x, y, z, t = symbols('x y z t')

# Définition du champ vectoriel V(x,y,z)
# Remplacez Vx, Vy, Vz par vos expressions exactes
Vx = t*y - z
Vy = -t*x + z
Vz = x - y
V = Matrix([Vx, Vy, Vz])

# Point O
O = Matrix([0, 0, 0])

# 1️⃣ V(O)
V_O = V.subs({x: 0, y: 0, z: 0})
print("Vecteur au point O :")
print(V_O)

# 2️⃣ Moment du torsor au point O
# Ici, M_O = r ∧ V, r = position vecteur, mais en O c'est 0
r = Matrix([x, y, z])
M = r.cross(V)
M_O = M.subs({x:0, y:0, z:0})
print("Moment au point O :")
print(M_O)

# 3️⃣ Vérification de l'antisymétrie du champ (∇V + ∇V^T = 0)
from sympy import diff, simplify
gradV = Matrix([
    [diff(Vx,x), diff(Vx,y), diff(Vx,z)],
    [diff(Vy,x), diff(Vy,y), diff(Vy,z)],
    [diff(Vz,x), diff(Vz,y), diff(Vz,z)]
])
antisym_check = simplify(gradV + gradV.T)
print("Vérification antisymétrie (doit être nul pour antisymétrie) :")
print(antisym_check)

# 4️⃣ Décomposition torsor = couple + glisseur
# Pour un torsor en O : T = (R, M_O)
# Ici, R = V_O, M_O déjà calculé
# Glisseur : translation parallèle à R
# Couple : reste du moment M_couple = M_O - O∧R (ici O=0 donc M_couple = M_O)
# Affichage
print("Résultat torsor :")
print("Résultante R =", V_O)
print("Moment M_O =", M_O)

# Note : Pour axe central, calcul plus détaillé selon formule :
# r_c = (R x M) / |R|^2
# (si R != 0)
          
