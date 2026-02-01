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





Jour 5 : PHP POO - Encapsulation
● Objectif du jour : Maîtriser les niveaux de visibilité (public, private, protected) et
l'utilisation des getters/setters.


● Questions Théoriques :
1. Qu’est-ce que l’encapsulation ? Quel est son but ?
L'encapsulation est un principe de la programmation oriente objet pour protege les donnees

2. Quelle est la différence entre public, private et protected ?
public les attributs et les methodes sont accessibles par tous les classe
private les attributs et les methodes sont accessibles seulement dans le meme classe actuelle
protected les attributs et les methodes sont accessibles seulement par les classe fille

3. À quoi servent les getters et setters ? Est-ce toujours nécessaire d'en avoir pour
chaque attribut ?
getters et setters des methodes pour acceder et modifier sur les attributs

● Challenges Pratiques :
1. Challenge 1 : Modifier la classe Voiture : mettre l'attribut vitesse en private.
class Voiture(){
    private $marque;
    private $modele;
    private $vitesse;

    public function accelerer(){
        $this->vitesse += 3
    }
    
}

2. Challenge 2 : Créer un getter getVitesse() et un setter setVitesse(int $v)
qui empêche d'assigner une vitesse négative.
class Voiture(){
    private $marque;
    private $modele;
    private $vitesse;

    public function accelerer(){
        $this->vitesse += 3
    }

    public function getVitesse(): int{
        return $this->vitesse;
    }

    public function setVitesse(int $v): void{
        if ($v < 0) {
            return;
        }
        $this->vitesse = $v;
    }
}

3. Challenge 3 : Créer une classe CompteBancaire avec un attribut solde privé.
Implémenter les méthodes deposer() et retirer() en s'assurant que le solde
ne puisse pas devenir négatif.

Class CompteBancaire{
    private $solde = 0;

    public function getSolde(){
        return $this->solde;
    }

    public function deposer(float $montant){
        if ($montant <= 0) {
            return;
        }

        $this->solde += $montant;
    }

    public function retirer(float $montant){
        if ($montant <= 0) {
            return;
        }

        if ($montant > $this->solde) {
            return;
        }

        $this->solde -= $montant;
    }
}

