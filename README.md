DURAND Maori 
LAFARGUE Pauline 

Algorithme programmation 
Rapport du projet de programmation – Sujet 1 
IVP1 S1 

       	Au travers de ce rapport nous allons vous présenter notre démarche lors de ce projet de programmation informatique visant à apprendre l’analyse de données. Celui-ci nous a permis d’appréhender l’utilisation du langage python, d’outils collaboratifs et le design d’algorithme, en manipulant des données liées à notre domaine d’études, le bâtiment. 
Tout d’abord, lors de ce travail nous avons décidé de travailler sur la plateforme en ligne Google Colab qui nous permettait d’écrire le code sans avoir besoin de télécharger de logiciel lourd. En effet l’un de nous a travaillé tout au long de ce projet sur un ordinateur de substitution, le sien étant en panne ; google colab était donc la seule option pour notre binôme. 

La première étape de ce projet étant de lire le fichier csv fournit, nous faisons le choix d’importer la bibliothèque pandas, une bibliothèque python qui nous permet de lire et analyser des données sous forme de DataFrames. Ainsi la première commande effectuée est « import pandas as pd ». Nous importons matplotlib, commande permettant de générer des graphiques via pandas. Nous importons le module datetime afin de manipuler les dates et les heures. 

1.	Lire les données 
Pandas nous permet de lire le fichier csv « post-32566-EIVP_KM.csv ». La fonction str nous permet ensuite de convertir les données « dates » et les données « heures » en chaînes. Puis nous utilisons la fonction send_at afin de diviser les données en plusieurs colonnes : une colonne pour la date de la donnée, une colonne pour l’heure et une pour le fuseau horaire. Nous transformons ensuite le format en format date et heure, puis avec la dernière ligne nous supprimons les deux colonnes inutiles. Pour afficher la courbe montrant l’évolution d’une variable en fonction du temps, nous introduisons ensuite une fonction « Choix_Date » qui prend en compte deux paramètres, « date_début » et « date_fin ». Cette fonction « choix date » n’a pas été évidente à intégrer, en effet en premier lieu nous avions fait l’erreur de considérer des arguments comme une chaîne de caractère, nous avions donc un problème après pour comparer les valeurs. La solution que nous avons adoptée est de considérer toutes les données du même jour en prenant le premier indice de ce jour et le dernier indice de ce jour, ce qui garantit d’avoir les données de la journée entière. Enfin, nous utilisons la fonction graphique qui prend la donnée choisie, la date début et la date fin. Nous utilisons matplotlib importé au début qui affiche la courbe d’évolution d’une variable choisie en fonction du temps. 

2.	Utiliser des fonctions statistiques 
Afin de trouver le minimum d’une des données du fichier, nous créons une variable mini, nous lui associons la valeur du premier élément de la liste de la donnée choisie. Puis cette variable mini parcours le data frame de la donnée choisie, et est comparée avec chaque élément du data frame. Si cet élément est inférieur à la variable mini, on l’affecte à mini. Ce qui nous donne le minimum de la liste de la donnée choisie. 

La méthode utilisée pour trouver le maximum d’une liste est la même, nous choisissons tout d’abord la donnée voulue, puis un intervalle de temps. Nous créons une variable maxi, nous lui associons la valeur du premier élément de la liste de la donnée choisie. Cette variable maxi parcours le data frame et est comparée à chaque élément de celui-ci. Si cet élément est supérieur à la variable maxi, on l’affecte à maxi. Nous obtenons ainsi le maximum. 

Afin d’utiliser les fonctions statistiques de la médiane, de l’écart-type, de la variance et de la moyenne, nous réalisons deux tris consécutifs des données : le premier sert à trier l’ensemble du data frame selon les dates, de la plus ancienne à la plus récente. La deuxième étape est de trier par heure. Ceci nous garantit un tri des données par ordre chronologique. Nous calculons ensuite la médiane de cette liste triée. Nous avons décidé de coder la première fonction puis d’implanter les fonctions statistiques suivantes par pandas afin de se concentrer sur un affichage graphique qualitatif par la suite. 

Pour l’affichage de l’écart-type, de la variance et de la moyenne, nous importons au préalable la fonction statistics de pandas ce qui nous permet d’utiliser les fonctions suivantes : std pour l’affichage de l’écart-type, var pour la variance et mean pour la moyenne arithmétique des données. Pour chacune des fonctions nous choisissons la variable et l’intervalle de temps pour lesquels nous voulons afficher la fonction. 

3.	Calculer l’indice de corrélation entre deux variables 
Pour déterminer la corrélation entre deux variables, nous calculons trois coefficients de corrélation différents. Nous calculons dans un premier temps le coefficient de Pearson, qui permet de calculer à quel point deux variables sont linéairement corrélées. Nous utilisons la notion de figure qui permet de regrouper les courbes de deux variables choisies sur un même graphique. Nous choisissons la première variable, à laquelle nous associons la couleur rouge ce qui va afficher sa courbe en fonction du temps en rouge. Nous choisissons la deuxième variable à laquelle nous associons la couleur bleue. Nous affichons les deux courbes sur le même graphique et nous calculons le coefficient de Pearson qui nous donne la corrélation linéaire entre ces deux variables, que nous affichons dans la légende. 
 

Puis nous répétons la même méthode de représentation des courbes en calculant cette fois-ci l’indice de corrélation de Spearman, qui permet d’estimer à quel point la corrélation entre deux variables peut être décrite par une fonction monotone. Il calcule la corrélation non linéaire de deux variables. La méthode est la même que précédemment, permettant d’afficher les courbes des deux variables sur le même graphique, et l’indice de corrélation de Spearman dans la légende du graphique. 

Nous répétons ensuite la même méthode d’application, cette fois-ci pour le calcul du coefficient de corrélation de Kendall entre deux variables, qui peut s’avérer plus pertinent que le coefficient de Spearman.  Le Tau de Kendall mesure la corrélation de rang entre deux variables. 

Ces trois coefficients de corrélation entre deux variables ont une valeur comprise entre -1 et 1. Dans le code il est possible d’en afficher la valeur dans la légende du graphique obtenu. 

4.	Calculer l’indice « humidex »
L’indice humidex est une formule qui prend en compte la chaleur et l’humidité d’un milieu afin de déterminer l’intensité de chaleur ressentie dans ce milieu. L’indice humidex s’exprime en fonction de la température de l’air de la pièce en degré Celsius, de l’humidité et du point de rosée en degré Celsius. Nous introduisons dans le code le calcul du point de rosée (ou température de rosée), qui correspond à la température à laquelle l’humidité se condense. Pour calculer le point de rosée, nous introduisons alpha, qui s’exprime en fonction de la température de l’air et de l’humidité. Nous choisissons un intervalle de temps où le calculer, nous prenons les valeurs de la température et de l’humidité qui correspondent à cet instant et nous calculons la valeur d’alpha. 
Puis pour le calcul du point de rosée, nous prenons la valeur du alpha trouvé puis nous associons au point de rosée noté T_rosee la formule pour le calculer en fonction de alpha. 
Enfin, pour le calcul de l’indice humidex, nous ressaisissons l’intervalle de temps étudié, nous prenons la valeur de la température de l’air à cet instant et la valeur trouvée pour le point de rosée à cet instant. Puis nous associons à l’indice humidex la formule pour le calculer : 
Humidex=T_air +0,5555 [6,11 x e^5417,7530((1/273,16) – (1/273,15+T_rosee)) – 10]
Nous calculons ainsi l’indice humidex à un instant donné. 

5.	Détection d’anomalies 
Afin de trouver d’éventuelles anomalies dans les données analysées, nous commençons par choisir une variable parmi celles étudiées, et un intervalle de temps. Nous prenons un intervalle de confiance de 15 valeurs à partir duquel nous affichons la médiane locale, la moyenne locale et l’écart-type local. Si une donnée au sein de cet intervalle est supérieure : (médiane locale + 0,5 x (écart-type local)) ou si une donnée est inférieure à : (médiane locale – 0,5 x (écart-type local)) alors cette donnée est considérée comme une anomalie. Nous superposons ensuite le graphique obtenu avec la fonction graphique sur la même période mais ne montrant que les anomalies, en créant un data frame (df.iloc[indices_anomalies]) avec uniquement les anomalies pour la variable choisie. Sur le graphique nous affichons les x en bleu, et le graphique montrant les anomalies en points rouges, grâce à l’argument « ro » dans la fonction plt.plot(). Les anomalies sont donc affichées sur le graphique par des points rouges. 

 

6.	Transfert du code en CLI 
Nous adaptons ensuite le code à un langage en CLI (Command-line interchange). En effet, afin de convertir le code en module et de s’en servir en tant que script, nous utilisons tout d’abord la fonction « main ». Puis, pour importer les fonctions nous utilisons le module « sys.arg » et nous appliquons cette méthode à l’intégralité de notre code afin de pouvoir le lire en tant que script. 

7.	Import du code sur Github 
Enfin, afin de créer un lien Github pour lire le code, nous avons créé un nouveau repository via github desktop avec notre code. Nous avons également converti le fichier word de ce rapport en fichier md afin de pouvoir le lire parallèlement au code. 

Conclusion 
Lors de ce projet la principale difficulté rencontrée fut le manque de cours d’algorithmique et de python, en particulier pour les étudiants bicursus qui, n’ayant jamais codé auparavant, se sont retrouvés sans suivi ou presque face à un projet complexe. Il fut difficile voire impossible d’apprendre à coder sur le tas en période de confinement, ce qui a pu mettre en difficulté certains binômes de projet. Aussi, le système de rendez-vous ponctuels en distanciel n’est ainsi peut-être pas la meilleure solution pour mener à bien ce projet. 










