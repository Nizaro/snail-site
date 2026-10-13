# Leçon P1 — Premiers pas en Python avec snAIl

![Des adolescents programmant snAIl en Python](../assets/images/snail_teenagers.jpeg){ width="380" align=right }

| | |
|---|---|
| **Parcours** | Python (13–17 ans) |
| **Durée** | 1 h 30 |
| **Effectif** | Binômes, 1 robot pour 2–3 binômes |
| **Prérequis** | Notions de base de Python (variables, boucles) |

## Objectifs

À la fin de la séance, les élèves savent :

- [ ] se connecter au robot depuis Python via son hotspot Wi-Fi ;
- [ ] commander une translation et une rotation ;
- [ ] lire une mesure de distance ultrason ;
- [ ] écrire une boucle « avance tant que la voie est libre ».

## Matériel

- 1 robot snAIl chargé pour 2–3 binômes (rotation des passages) ;
- 1 ordinateur par binôme avec Python 3 et la bibliothèque snAIl installés ;
- un obstacle (carton, boîte) par poste.

## Déroulé

### 1. Du bloc au code (10 min)

Rappel pour ceux qui viennent du parcours blocs : chaque bloc correspond à une ligne de code. Montrer côte à côte un programme en blocs et son équivalent Python.

### 2. Connexion et premier script (25 min)

Connecter l'ordinateur au Wi-Fi du robot, puis :

```python
from snail import Robot

robot = Robot()          # connexion via le hotspot
robot.avancer(0.5)       # translation : 50 cm
robot.tourner(90)        # rotation : 90 degrés
robot.avancer(0.5)
```

Chaque binôme modifie les valeurs et observe. **Prédire avant d'exécuter**, comme au parcours blocs.

### 3. Lire un capteur (20 min)

```python
distance = robot.ultrason()   # distance à l'obstacle, en mètres
print(f"Obstacle à {distance:.2f} m")
```

Mesurer la distance à un carton, le rapprocher, mesurer encore. Discussion : précision, limites du capteur.

### 4. Défi : s'arrêter avant l'obstacle (25 min)

Écrire une boucle qui fait avancer le robot **tant que** la voie est libre, et l'arrête à 20 cm de l'obstacle :

```python
while robot.ultrason() > 0.20:
    robot.avancer_un_peu()
robot.stop()
```

Les plus rapides : faire contourner l'obstacle (rotation, avance, rotation inverse).

### 5. Bilan (10 min)

Démonstrations. Ouverture : *« Et si le robot utilisait sa caméra 3D au lieu des ultrasons ? »* — c'est le sujet des leçons de vision.

!!! note "Pour l'enseignant"
    Les noms de fonctions (`avancer`, `tourner`, `ultrason`…) sont à adapter à l'API réelle de la bibliothèque snAIl ; la structure de la séance ne change pas.
