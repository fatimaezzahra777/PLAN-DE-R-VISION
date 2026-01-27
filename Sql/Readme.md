1. Quelle est la différence entre DDL (CREATE, ALTER) et DML (INSERT, UPDATE,
DELETE) ?
DDL c'est data definition language pour definie ou modifier la structure de la basede donnees et il ne manipule pas directement les données
DML c'est data manipulation language pour manipule les données à l'intérieur des tables.

2. À quoi sert une clé primaire ?
La clé primaire est un attribut unique et not null qui permet d'identifier chaque enregistrement sans duplication et Cet attribut est obligatoire.

3. Comment filtre-t-on des données avec la clause WHERE ?
La clause where dans sql pour filtrer les lignes d'un table



Challenges Pratiques :
1. Challenge 1 : Écrire la requête CREATE TABLE pour une table Produits (id, nom,
prix, stock).

CREATE TABLE Produits (
    id int PRIMARY KEY,
    nom varchar(100) NOT NULL,
    prix decimal(10,2) NOT NULL,
    stock int NOT NULL 
);

2. Challenge 2 : Écrire les requêtes INSERT pour ajouter 3 nouveaux produits dans
la table.

INSERT INTO Produits (nom, prix, stock)
VALUES
('pc', 3000, 100),
('chargeur', 300, 50),
('Sac', 200, 50);

3. Challenge 3 : Écrire une requête UPDATE pour augmenter le prix d'un produit
spécifique de 10%, puis une requête DELETE pour supprimer un produit en
rupture de stock

UPDATE Produits
SET prix = prix * 1.10
WHERE prix = 200;


DELETE FROM Produits
WHERE id = 3;
