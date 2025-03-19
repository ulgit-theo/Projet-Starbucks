# Projet-Starbucks
<h1> Contexte </h1>

1) Contexte :
Starbucks est une chaîne de cafés américaine fondée à Seattle. Elle propose à la fois des boissons et de la nourriture.

2) Contenu :
Ce jeu de données contient les informations nutritionnelles des produits alimentaires et des boissons proposés par Starbucks. Toutes les informations nutritionnelles pour les boissons correspondent à une portion de 12 oz (soit environ une canette de soda de 33 centilitres)



<h1> Les étapes du Projet </h1>

<b> Import des données </b>
- On utilise genfromtxt pour importer les données du fichier starbucks-menu-nutrition-drinks.csv.



<b> Data Cleaning</b>
- Les données manquantes ont été symbolisées par des "-". On Remplace ces valeurs par des valeurs nulles (nan)
- Nous allons séparer les différents types de données. "header" contiendra les entête de colonne, "drinks" le nom des boissons et "data" les données numériques.
- Certaines boisson n'avais aucune donnée numériques. A l'aide de la méthode np.isnan(...).all(...), on calcule la part des boissons sans donnée. 

<b> Analyse des données </b>

- Calcule de la moyenne des calories par boisson
- Calcule de la médiane des protéines
- Calcule du   maximum et du minimum des lipides (fat)
- idenfication de la boisson avec le maximum de calories (nom de la boisson + nombre de calories)
- Identification de la boisson avec le minimum de calories (nom de la boisson + nombre de calories)

<b> Data modeling </b>

Afin de simplifier la lecture et l'analyse des boissons, nous souhaitons créer un "NutriScore" permettant d'indiquer rapidement le niveau de calorie d'une boisson : 
- de 0 à 100 calories, la boisson aura le niveau 1
- de 100 à 200 calories, niveau 2
- de 200 à 300 calories, niveau 3
- 300 et plus, niveau 4

