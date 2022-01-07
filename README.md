# projet_fde
Projet fin d'études: La complexité de la requête SQL
## Lien sur le travail personel
https://colab.research.google.com/drive/1_BBbWTCLNnQ8kdgBPNskDp41hYCHM8fy?usp=sharing
## Description du sujet de projet 
Ce projet porte sur l’étude de clusters d’explorations d’analyse de données, avec l’objective de les expliquer, cette à dire, de trouver qu’est qu’on en commun ces explorations, qui fait qu’elles soient groupées ensemble. On s’intéresse particulièrement à la complexité des requêtes. 
Une exploration de données est une séquence de requêtes d’analyse sur une base de données. Dans nos premiers travaux, on s’est intéressé aux opérations réalisées dans ces requêtes. Par exemple, considérez l’exploration suivante, composée de 4 requêtes : 
− q1: SELECT species FROM All3col; 
− q2: SELECT species FROM All3col WHERE longitude < 0; 
− q3: SELECT species, longitude, latitude FROM All3col; 
− q4: SELECT species, longitude FROM All3col ORDER BY species; 
La requête q1 projette un attribut d’une table ; q2 ajoute un filtre ; q3 enlève le filtre et projette 2 attributs supplémentaires, q4 enlève une projection et ajoute une clause d’ordre. 
Dans ce contexte, 10.668 requêtes SQL, concernant 2.809 explorations, réalisés par 97 utilisateurs sur la plateforme SQLShare, ont été parsées afin d’obtenir les clauses principales (projections, sélections, tables, agrégations, groupements et ordre) et de calculer les opérations réalisées [1]. Les explorations ont ensuite été comparés avec une distance d’édition contextuelle et organisées en clusters avec un algorithme de clustering agglomératif [2]. Une étude préliminaire des clusters, avec des nombreux indicateurs statistiques et visuelles, a permis de tirer plusieurs observations sur des styles d’analyse et les compétences des utilisateurs qui les ont réalisées. Par exemple, certaines explorations sont longues et enchainent des changements dans les attributs projetés ou les filtres, d’autres sont plus courtes mais avec beaucoup de modifications entre une requête et la suivante, encore d’autres manifestent des comportements singuliers. Ces observations sont résumées dans le tableau 4 de [2]. 
Une vidéo résumant le travail réalisé est disponible sur : https://www.youtube.com/watch?v=BY88D7Xqllo 
Ensuite, nous nous sommes intéressés à la complexité des requêtes (longueur de requêtes et usage de clauses avancées) [3]. 
Dans ce projet, nous nous voulons aller plus loin dans l’analyse de la complexité des requêtes afin de mieux classifier les compétences des utilisateurs. 
La première partie du projet sera dédié à l’étude d’indicateurs pour mesurer la complexité d’une requête SQL et juger lesquels sont applicables aux requêtes de SQLShare. Les travaux préliminaires de Jain et al. [4,5], ainsi que nos travaux en cours [3] constituent un bon point de départ. 
Ces indicateurs serviront ensuite à comprendre et à expliquer les comportements typiques des utilisateurs. La deuxième partie consiste à appliquer les indicateurs retenus lors de la première partie afin d’expliquer les 12 clusters d’explorations issues de SQLShare [3]. Les résultats seront restitués sous la forme d’indicateurs statistiques et visuels, pouvant s’inspirer des indicateurs décrits dans [3]. 
## Contributions attendues 
• État de l’art sur les indicateurs permettant de mesurer la complexité d’une requête SQL. • Expérimentation avec 12 clusters d’explorations de SQLShare. 
• Présentation des résultats via des indicateurs statistiques et visuels. 
