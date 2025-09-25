# 🚇 Projet Itinéraire Métro

Un programme en **C** permettant de calculer l'itinéraire le plus court
entre deux stations de métro, en utilisant l'algorithme de **Dijkstra**.

Le projet utilise un fichier CSV (`metro_modifiee.csv`) décrivant les
lignes, stations et horaires, et propose une interaction via le terminal
pour rechercher et afficher le chemin optimal.

------------------------------------------------------------------------

## 📂 Structure du projet

-   `ItineraireMetro.c` : Code source principal du projet (structures,
    gestion des lignes/stations, algorithme de Dijkstra, interface
    utilisateur).
-   `metro_modifiee.csv` : Données du réseau de métro (stations,
    horaires des premiers et derniers trains).
-   `LICENSE.txt` : Licence du projet (**MIT**).

------------------------------------------------------------------------

## ⚙️ Compilation

Compiler le projet avec **gcc** (ou un compilateur C compatible) :

``` bash
gcc -o ProjetMetro ItineraireMetro.c
```

------------------------------------------------------------------------

## ▶️ Exécution

Le programme s'exécute en ligne de commande :

``` bash
./ProjetMetro pathFinder metro_modifiee.csv
```

### Exemple sous Windows

``` powershell
ProjetMetro.exe pathFinder metro_modifiee.csv
```

⚠️ Assurez-vous que le fichier `metro_modifiee.csv` se trouve dans le
**même dossier** que l'exécutable.

------------------------------------------------------------------------

## 🖥️ Utilisation

Une fois lancé, le programme propose un menu interactif :

1.  Tapez `1` pour rechercher un itinéraire.
2.  Entrez la **station de départ**.
3.  Entrez la **station d'arrivée**.
4.  Le programme calcule et affiche :
    -   L'heure de départ et d'arrivée.
    -   Les lignes à emprunter.
    -   Les correspondances éventuelles (+5 min ajoutés).
    -   Le temps total de trajet.

Exemple de sortie simplifiée :

    ----------------------------------------------------------
    Départ : 14:30         Arrivée : 14:50
    Itinéraire trouvé (20 min) :
      - Quitter la station CHÂTELET (Ligne 1)
      - Correspondance : Ligne 4
      - Arrivée à GARE DU NORD
    ----------------------------------------------------------

------------------------------------------------------------------------

## 🧮 Fonctionnalités principales

-   Lecture du réseau depuis `metro_modifiee.csv`.
-   Structures de données pour représenter :
    -   Stations
    -   Lignes
    -   Réseau complet (graphe)
-   Calcul du plus court chemin avec **Dijkstra**.
-   Gestion des correspondances avec pénalité (+5 minutes).
-   Interaction simple via le terminal.

------------------------------------------------------------------------

## 📜 Licence

Projet distribué sous licence **MIT**.\
Voir le fichier [LICENSE.txt](LICENSE.txt) pour plus de détails.
