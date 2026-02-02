    Jour - 1

1. Qu'est-ce qu'une classe dans un diagramme de classes ?
Une classe dans un diagramme de classe est une modele qui contient des attributs et des methodes.

2. Pourquoi est-il problématique d'avoir des classes sans méthodes ?
La problématique d'avoir des classes sans méthodes cette classe ne fait aucune action

3. Expliquer le principe de responsabilité unique.
le principe de responsabilité unique (SRP) c'est le premier principe de SOLID une classe doit avoir une seule raison de changer


Challenges Pratiques :
1. Challenge 1 : Créer une classe Livre avec uniquement des attributs (titre,
auteur, isbn). Puis, la critiquer.
-Pour la classe livre est bien definie mais il a besoin des methodes

2. Challenge 2 : Refactoriser la classe Livre en ajoutant les méthodes
essentielles (emprunter(), retourner(), afficherDetails()).

3. Challenge 3 : Modéliser une classe Etudiant et une classe Cours. 
Placer
correctement la méthode inscriptionAuCours() dans la classe la plus
pertinente et justifier le choix.
-J'ai ajouté la methode inscriptionAuCours() dans la classe etudiant car il est celui qui s'inscrit dans le cours



Jour 6 : UML - Relations entre Classes
● Objectif du jour : Différencier et utiliser correctement les relations (Association,
Agrégation, Composition) et les cardinalités.

● Questions Théoriques :
1. Quelle est la différence fondamentale entre la composition et l'agrégation ?
Donnez un exemple pour chacune.
la composition est une relation forte entre deux classe si supprimer l'objet principal l'autre classe ne travaille pas.
L'agrégation c'est une relation faible entre deux classe

2. Comment lisez-vous une cardinalité (ex: 1..* des deux côtés) ?
1 ou plusieurs 
1 c'est le minimum
* c'est le maximum

3. Qu'est-ce qu'une classe associative et quand l'utilise-t-on ?
Une classe associative est une classe placée sur une association entre deux classes

● Challenges Pratiques :
1. Challenge 1 : Modéliser la relation entre Maison et Piece. Justifier le choix entre
agrégation et composition.
La relation est composition car une piece ne peux pas execute sans maison

2. Challenge 2 : Modéliser la relation entre Etudiant et Cours. Définir les
cardinalités (un étudiant peut suivre plusieurs cours, un cours a plusieurs
étudiants).
3. Challenge 3 : Le diagramme actuel montre une relation incorrecte (ex:
composition au lieu d'association simple). Identifier l'erreur, la corriger et
justifier la correction.