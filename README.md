# Compter les Clics !

## Description du projet
"Compter les Clics !" est un jeu interactif en ligne où le joueur doit cliquer le plus rapidement possible sur un bouton pendant un temps défini. Le but est de battre son propre record et de maximiser son score. Le jeu intègre des effets visuels (animations, glow néon, pop-up +1), des sons, et un tableau des meilleurs scores persistants grâce au stockage local.

---

## Technologies utilisées
- **HTML5** : structure du contenu
- **CSS3** : styles, animations, dégradés, effets néon et responsive design
- **JavaScript (ES6)** : logique du jeu, gestion des scores, minuteur, sons, stockage local (`localStorage`)

---

## Fonctionnalités principales
- Sélecteur de durée de partie (10s, 20s, 30s)
- Score en temps réel avec animations de pulsation
- Pop-up "+1" à chaque clic
- Tableau des meilleurs scores persistant
- Minuteur avec avertissement visuel lorsque le temps est presque écoulé
- Sons pour chaque clic et fin de partie
- Explications du jeu de manière ludique
- Effets graphiques interactifs : fond animé, glow néon, responsive design

---

## Lien vers la page GitHub Pages
[Voir le rendu final sur GitHub Pages](https://habairi-med-dawsser.github.io/habairi_med_dawsser_Jeu_Compter_les_Clics/)  

---

## Nouveautés explorées / Ce que j’ai appris
- Animation de texte et éléments via CSS (`@keyframes`, `transform`, `opacity`)  
- Gestion d’événements complexes en JavaScript pour le clic et le timer  
- Manipulation du DOM pour créer et supprimer dynamiquement des éléments (`+1` pop-up)  
- Stockage local avec `localStorage` pour garder les meilleurs scores  
- Synchronisation du timer et du score en temps réel  
- Optimisation du code pour les effets visuels et sonores  
- Adaptation responsive pour différents écrans et tailles de fenêtre  

---

## Difficultés rencontrées
1. **Gestion du temps et synchronisation du timer**  
   - Maintenir un compte à rebours précis sans bloquer le reste du jeu.  

2. **Désactivation et réactivation des éléments**  
   - Éviter que le joueur change la durée de la partie ou clique sur le bouton de manière intempestive pendant le jeu.  

3. **Stockage et récupération des meilleurs scores**  
   - Gérer correctement `localStorage` pour différentes durées de partie et afficher les valeurs de manière fiable.  

4. **Animations et effets visuels**  
   - Faire en sorte que la pulsation du score et le pop-up "+1" apparaissent de manière fluide et n’interfèrent pas entre eux.  

5. **Responsive design / compatibilité mobile**  
   - Adapter le fond animé, le tableau, le texte explicatif et les boutons pour les petits écrans.  

6. **Gestion des sons**  
   - Prévoir que la lecture des sons puisse être bloquée par certains navigateurs (autoplay).  

---

## Solutions apportées
1. **Timer et synchronisation**  
   - Utilisation de `setInterval` et réinitialisation du timer à chaque nouvelle partie pour éviter les conflits ou doubles intervalles.  

2. **Désactivation / réactivation**  
   - Le select et le bouton sont désactivés pendant la partie et réactivés à la fin avec `disabled = true/false`.  

3. **Stockage des scores**  
   - Lecture et écriture dans `localStorage` avec des valeurs par défaut (`|| 0`) pour garantir que le tableau des meilleurs scores soit toujours correct.  

4. **Animations fluides**  
   - Utilisation de `classList.add/remove` pour déclencher les animations CSS.  
   - Nettoyage des pop-ups "+1" via `animationend` et `setTimeout` pour éviter l’accumulation dans le DOM.  

5. **Responsive design**  
   - Ajout de `@media queries` pour adapter la taille des boutons, du tableau et du texte explicatif sur petits écrans.  

6. **Gestion des sons**  
   - Ajout de `try/catch` lors de la lecture des sons pour éviter que le jeu plante si l’autoplay est bloqué par le navigateur.  
