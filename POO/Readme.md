Jour 4 : PHP POO - Classes & Objets
● Objectif du jour : Comprendre la syntaxe de base pour créer une classe, définir ses
membres et l'instancier.

● Questions Théoriques :
1. Quelle est la différence entre une classe et un objet ?
classe : C'est un modele qui contient les attributs et les methodes.
Objet : c'est l'instanciation d'un classe


2. À quoi sert le mot-clé $this ?
Le mot clé $this pour pour accedée a les attributs et les methodes dans ce classe courant

3. Quel est le rôle du constructeur (__construct) ?
constructeur est une methode speciale pour preparer l'objet s'execute automatiquement si on creer un objet


● Challenges Pratiques :
1. Challenge 1 : Créer une classe Voiture avec 3 attributs (marque, modele,
vitesse) et une méthode accelerer() qui augmente la vitesse.
class Voiture(){
    private $marque;
    private $modele;
    private $vitesse;

    public function accelerer(){
        $this->vitesse += 3
    }
}
2. Challenge 2 : Ajouter un constructeur à la classe Voiture pour initialiser la
marque et le modèle lors de la création de l'objet.

public function __construct($marque, $modele){
    $this->marque = $marque;
    $this->modele = $modele;
}


3. Challenge 3 : Instancier deux objets de la classe Voiture et appeler leurs
méthodes pour vérifier leur fonctionnement.

$voiture1 = new Voiture("Bmw", 10);
$voiture2 = new Voiture("BMW", 5);

$voiture1->accelerer();
$voiture1->accelerer();
