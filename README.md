
# Test technique HCNX ⚡️

Nous venons de signer un nouveau contrat avec un client : une ONG.
 
Cette ONG souhaite travailler avec nous dans le cadre du Don par SMS et possède un historique de DON qu’elle a exporté via la solution de l’ancien prestataire : un fichier CSV de presque 1 million de lignes.
 
Notre objectif est d’interconnecter cette ONG à notre plateforme et pour cela nous avons besoin que tu intègres sa « data » dans une base de données MySQL.



Le fichier CSV est structuré de la manière suivante : 1 ligne = 1 don
 

| DATE | MONTANT | TELEPHONE | CODE POSTAL |
|---|---|---|---|
| Date et heure du don | Montant du don <br /> en euro pour chaque ligne | numéro de téléphone portable de l’utilisateur<br> (c’est sur cette colonne que nous souhaitons dé doublonner) | code postale de l’utilisateur |

## 🥇 Tache 1
###  ⛔️ Restriction : 
- ORM interdit


### 🎯 objectif : 

Développer un script PHP a l'aide du composant COMMAND de Symfony afin de traiter et d’intégrer la donnée dans une Base de données MySQL (ORM interdit)


#### 🔍 Détail :
Construire une table qui te parait la plus judicieuse possible qui permet d’agréger le montant des dons par numéro de téléphone.
A minima, il doit y avoir ces 2 colonnes :
- le numéro de téléphone
- le montant total des dons pour ce numéro de téléphone
 
Ensuite, construire une deuxième table afin d’agréger les codes postaux par numéro de téléphone
A minima, il doit y avoir ces 2 colonnes :
- le numéro de téléphone
- le code postal pour ce numéro de téléphone
 
Dans les 2 cas, j’impose d’avoir des clés uniques :
- premièrement sur le numéro de téléphone
- deuxièmement sur le couple numéro de téléphone et code postal
## 🥈 Tache 2

### ⛔️ Restriction : 
- ORM autorisé
- Librairie JS a utiliser : [ChartJs](https://www.chartjs.org/docs/latest/)


### 🎯 objectif : 

Créer une vue nommée : « Dashboard ».
Ce dashboard permet de visualiser sous forme de graphiques la data intégrée dans la base de données.


#### 🔍 Détail :
J’aimerai avoir un Bar Chart avec les caractéristiques suivantes :
- en abscisse : les montants des dons
- en ordonnée : le nombre de personnes uniques ayant donné le montant en abscisse
 
Puis j’aimerai avoir un Pie chart indiquant les 10 départements pour lesquels il y a le plus de donateurs uniques. Le 11eme segment sera le total de tous les autres départements.
 
## 🚦 Les Pré-requis

- PHP >= 7.3
- Symfony >= 5.4
- MySql
- Il est aussi conseillé de faire un maximum de commit pour bien détailler les étapes de votre raisonnement au cours du développement.
- Le temps est libre mais il est tout de même conseillé de passer moins de 8h sur le sujet (temps de setup d'environnement compris)
- ORM interdit pour la tache 1


## 🎁 Bonus

Toutes les fonctionnalités que vous aurez le temps d'ajouter seront bonnes à prendre. Soyez créatifs !!
