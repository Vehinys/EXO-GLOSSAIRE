# GLOSSAIRE
Pour visualiser cette documentation sur VSCode 
```
CTRL + SHIFT + V
```

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général

1.	<b> Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte :</b>

- Il est nécessaire d'avoir un serveur web local qui prend en charge PHP et une base de données.
- Laragon & WampServer

2.	<b>Qu’est-ce qu’un algorithme ? </b>

- C'est des instructions pour accomplir une tâche spécifique.

3.	<b>Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ? </b>

- Une variable est un stockage qui contient une valeur pouvant être modifiée. 
- Son préfixe est le symbole $.

4.	<b>Qu’est-ce que la portée d’une variable ? </b>

- C'est la zone de code où elle a été déclarée.

5.	<b>Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ? </b>

- Une constante est une valeur qui ne peut pas être modifiée.
- Une variable peut être modifiée.

6.	<b>Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation : </b>

- Les variables internes qui sont toujours disponibles, quel que soit le contexte
- 9 Superglobale 
- $_GET

7.	<b>Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur) : </b>

- int : $a = 123;
- float : $b = 12.34;
- string : $c = "Hello";
- bool : $d = true;
- array : $e = array(1, 2, 3);

8.	<b>Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ? </b>

- Oui,

- Tableaux indexés : Pour des indices numériques.
- Tableaux associatifs : Pour des chaînes de caractères.

9.	<b>Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles : </b>

// <b>Conditionnelle (if, else if, else) :</b>

- // if, Else if, else
      ($a > $b) {
         echo "a est plus grand que b";
    } elseif ($a == $b) {
         echo "a est égal à b";
    } else {
         echo "a est plus petit que b";
    }

// <b>Boucles (for, while, foreach) :</b>

- // for
     for ($i = 0; $i < 10; $i++) {
        echo $i;
     }

- // while 
        $i = 0;
    while ($i < 10) {
        echo $i;
        $i++;
    }

- // foreach
    $arr = array(1, 2, 3, 4);
    foreach ($arr as $value) {
        echo $value;
    }

10.	<b>Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ? </b>

- strlen

11.	<b>Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP </b>

- Une session est un moyen de stocker des informations sur l'utilisateur à travers plusieurs pages d'un site web, 
  et la fonction pour démarrer une session en PHP est session_start(), par exemple, 
  on peut démarrer une session et définir une variable de session avec session_start(); $_SESSION["username"] = "JohnDoe";.

12.	<b>Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP </b>

- Un cookie est un petit fichier stocké sur l'ordinateur de l'utilisateur par un site web pour mémoriser des informations entre les sessions,
  on peut créer un cookie avec setcookie("user", "John Doe", time() + (86400 * 30), "/") et le lire avec $_COOKIE["user"].

13.	<b>Quelle est la différence entre les instructions « require » et « include » en PHP </b>

- require est utilisé lorsque le fichier est obligatoire pour l'application.
- require arrête l'exécution à la ligne où l'erreur est produite.

- include est utilisé lorsque le fichier n'est pas nécessaire.
- include continue à s'exécuter malgré les erreurs.

14.	<b>Comment effectuer une redirection en PHP ? </b>

- header (Location : '...')
- Créer une fonction Redirection

15.	<b>Définir la partie « front-end » et « back-end » d’une application </b>

- "Front-end" : c'est la partie graphique et l'experience utilisateur.
- "back-end"  : c'est la partie devellopement web coté serveur qui n'est pas visible par les utilisateurs.

16.	<b>Définir le contrôle de version ? Qu’est-ce que Git ? </b>

- Le contrôle de version est un système qui permet de suivre et gérer les modifications apportées aux fichiers au fil du temps, 
  et Git est un outil distribué de contrôle de version qui facilite la collaboration et la gestion efficace des versions de projets logiciels.

17.	<b>Qu’est-ce qu’un CMS ? Citer au moins 2 exemples </b>

- C'est un logiciel qui permet de créer et gérer un site Web sans coder.
- Wordpress & joomla



## Front-end

18.	<b>Définir HTML</b>

- HTML : (HyperText Markup Language) est un langage informatique utilisé pour créer des pages web. 
  Il repose sur un système de balises permettant de formater le texte, 
  insérer des éléments interactifs comme des images et des liens, et définir la structure d'une page web

19.	<b>Définir CSS</b>

-  CSS (Cascading Style Sheets en anglais, ou « feuilles de style en cascade ») permet d'appliquer 
   des styles différents éléments selectionnés dans un document HTML.

20.	<b>Définir Javascript</b>

-  Javascript est un langage de programmation qui permet de créer du contenu mis à jour de façon dynamique, 
   de contrôler le contenu multimédia, d'animer des images.


21.	<b>Définir JSON. Dans quel contexte ce format est-il utilisé ? </b>

-

22.	<b>Peut-on interpréter du Javascript côté serveur ? Si oui, comment ? </b>

- 

23.	<b> Qu’est-ce qu’un sélecteur CSS ? </b>

- Un sélecteur est une expression qui permet de cibler un ou plusieurs éléments HTML dans une page. 
  Il indique au navigateur quels éléments doivent être stylisés en fonction des règles CSS associées.

24.	<b> Quelle balise HTML permet de créer un lien hypertexte ? </b>

- < a href="adresse de redirection" > texte cliquable à afficher < /a >

25.	<b> Qu’est-ce qu’une requête AJAX ? </b>

- Une requête AJAX (Asynchronous JavaScript and XML) est une technique permettant à une page web 
  de communiquer avec un serveur en arrière-plan et de mettre à jour dynamiquement son contenu 
  sans nécessiter de rechargement complet de la page.

26.	<b>Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?</b>

- .nomdeclasse { déclarations CSS }

27.	<b>Définir le responsive design</b>

- Le responsive design est une methode qui adapte automatiquement une page web selon l'orientation et la resoltion de l'ecran utilisé.

28.	<b>Qu’est-ce que le templating ?</b>

- 

29.	<b>Qu’est-ce qu’une fonction anonyme en Javascript ?</b>

- 

30.	<b>Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?</b>

-

31.	<b>Qu’est-ce qu’un « media query » ?</b>

- Les requêtes média (media queries) permettent de modifier l'apparence d'un site en fonction du type d'appareil (mobile, tablette, Pc portable,...)

32.	<b>Qu’est-ce qu’un pseudo élément en CSS ?</b>

- Un pseudo-élément est un mot-clé ajouté à un sélecteur qui permet de mettre en forme certaines parties de l'élément ciblé par la règle.

33.	<b>Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent</b>

- C'est un framework CSS gratuit et open-source.

- Materialize
- Tailwind CSS


34.	<b>Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes</b>

-
-

## UX UI

35.	<b>Quelle est la différence entre UX Design et UI Design ?</b>

-

36.	<b>Qu’est-ce qu’un wireframe ? </b>

-

37.	<b>Qu’est-ce qu’un prototype ? </b>

-

38.	<b>Qu’est-ce que la hiérarchie visuelle en UI Design ?</b>

-

39.	<b>Qu’est-ce que l’accessibilité en UX Design ? </b>

-

40.	<b>Qu’est-ce qu’une grille de mise en page ?</b>

-

41.	<b>Qu’est-ce que la notion d’affordance en UX Design ?</b>

-

42.	<b>Qu’est-ce qu’un « mobile first design » ?</b>

- C'est la création dun projet web / web mobile qu'on commence par moble puis par ordinateur.

43.	<b>Donner une définition de la programmation orientée objet </b>

- 

44.	<b>Qu’est-ce qu’une classe ? Comment la déclare-t-on ?</b>

-

45.	<b>Qu’est-ce qu’un objet ?</b>

-

46.	<b>Définir la notion de propriété / attribut / méthode</b>

-

47.	<b>Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité</b>

-

48.	<b>Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?</b>
-

49.	<b>Qu’est-ce que l’encapsulation ?</b>

-

50.	<b>Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple</b>

-

51.	<b>Définir l’opérateur de résolution de portée</b>

-

52.	<b>Définir une méthode / propriété statique</b>

-

53.	<b>Définir le polymorphisme en POO</b>

-

54.	<b>Définir une méthode / classe abstraite ?</b>

-

55.	<b>Définir le chaînage de méthodes</b>

-

56.	<b>Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »</b>

-

57.	<b>Qu’est-ce qu’un « autoload » ?</b>

-

58.	<b>Comment appelle-t-on en français les « getters » et les « setters » ?</b>

-

59.	<b>Qu’est-ce que la sérialisation en PHP ? </b>

-


## Architecture 

60.	<b>Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. 
       Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence</b>

- 
- 

61.	<b>Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern</b>

-

-
-
-

62.	<b>Qu’est-ce que l’architecture MVC ?</b>

-

63.	<b>Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?</b>

-

64.	<b>Quels sont les avantages de l’architecture MVC ?</b>

-

65.	<b>Existe-t-il des variantes à l’architecture MVC ?</b>

-

66.	<b>Qu’est-ce qu’une API ? Définir l’architecture REST</b>

-


## Modélisation - Base de données

67.	<b>Qu’est-ce que la modélisation de données ? Définir la méthode Merise</b>

68.	<b>Quelles sont les 3 étapes principales de la méthode Merise ? </b>
- a. <b>Analyse, conception et réalisation</b>
- b. <b>Planification, exécution et contrôle</b>
- c. <b>Création, modification et suppression</b>
69.	<b>Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?</b>

- Le Modèle Conceptuel de Données (MCD) est une représentation abstraite des données nécessaires au système d'information, 
  décrivant les entités, leurs attributs, et les relations entre elles, indépendamment des contraintes techniques.

70.	<b>Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?</b>

- Le Modèle Logique de Données (MLD) est une représentation détaillée et structurée des données qui précise 
  les tables, les colonnes, et les clés nécessaires pour implémenter le Modèle Conceptuel de Données (MCD) 
  dans un système de gestion de base de données relationnelle, tout en tenant compte des contraintes logiques et de la normalisation.

71.	<b>Donner la définition des mots suivants :</b>

- a. <b>Entité</b>

-

- b. <b>Relation</b>

-

- c. <b>Cardinalité</b>

-

- d. <b>Clé primaire / clé étrangère</b>

-

72.	<b>Que devient une relation de type « Many To Many » dans le modèle logique de données ?</b>

-

73.	<b>Qu’est-ce qu’une base de données ?</b>

-

74.	<b>Définir les notions suivantes : </b>

-

- a. <b>SQL :</b>

-

- b. <b>MySQL :</b>

-

- c. <b>SGBD (donner 2 exemples de SGBD) :</b>

-

75.	<b>Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de lignes appelées ___ et de colonnes appelées ___</b>

-

76.	<b>Quelle est la différence entre une base de données relationnelle et non relationnelle ?</b>

-

77.	<b>Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?</b>

-

78.	<b>A quoi sert une vue dans une base de données ?</b>

-

79.	<b>Qu’est-ce que l’intégrité référentielle dans une base de données ?</b>

-

80.	<b>Quelles sont les fonctions d’agrégation en SQL ?</b>

-

81.	<b>Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?</b>

-

82.	<b>Quelles sont les clauses qui permettent de :</b>

- a. <b>Insérer un nouvel enregistrement dans une table :</b>

- On utilise la commande INSERT INTO

- b. <b>Modifier un enregistrement dans une table :</b>

- On utilise la commande UPDATE

- c. <b>Supprimer un enregistrement dans une table :</b>

- On utilise la commande DELETE

- d. <b>Supprimer la base de données :</b>

- On utilise la commande DROP DATABASE

- e. <b>Filtrer les résultats d’une requête SQL :</b>

- On utilise la clause WHERE

- f. <b>Trier les résultats d’une requête SELECT :</b>

- On utilise la clause ORDER BY

- g. <b>Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique :</b>

- On utilise la clause GROUP BY

- h. <b>Concaténer 2 chaînes de caractères :</b>

- SELECT CONCAT(nom, prenom) AS ensembleNomPrenom

83.	<b>Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?</b>

- En utilisant Laragon, pour se connecter à une base de données en PHP, j'utilise la classe native PDO (PHP Data Objects) 
  en definisant dans mon ficher DAO les informations suivantes : 

  $host = 'localhost';
  $username = 'nom_utilisateur';
  $password = 'mot_de_passe';
  $database = 'nom_de_la_base_de_donnees';

## Symfony

84.	<b>Qu’est-ce que Symfony ?</b>

-

85.	<b>Sur quel langage de programmation et design pattern repose Symfony ? </b>

-

86.	<b>Quelle est la dernière version en date de Symfony ?</b>

- La dernière version de Symfony, en date de juillet 2024, est la version 7.1.3​

87.	<b>Qu’est-ce qu’un bundle ? </b>

-

88.	<b>Quel est le moteur de template utilisé par défaut dans Symfony ?</b>

-

89.	<b>Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?</b>

-

90.	<b>Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?</b>

-

91.	<b>Que permet le bundle Maker au sein de Symfony ? </b>

-

92.	<b>Quel est le langage de requêtage exploité au sein d’un projet Symfony ?</b>

-

93.	<b>Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?</b>

-


## Sécurité

94.	<b>Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?</b>

- L'injection SQL est une attaque où un pirate envoie des commandes malveillantes à une base de données à travers des formulaires ou des champs de saisie sur un site web. 
  Cela peut  leur permettre de voler des informations ou d'altérer la base de données.

- Vérifier et nettoyer toutes les données que les utilisateurs entrent dans les formulaires, autant côté serveur que côté client.


95.	<b>Qu’est-ce que la faille XSS ? Comment s’en prémunir ?</b>

- Cross-site scripting (XSS) est une faille de sécurité qui permet à un attaquant d'injecter dans un site web un code client malveillant. 
  Ce code est exécuté par les victimes et permet aux attaquants de contourner les contrôles d'accès et d'usurper l'identité des utilisateurs. 

- L’encodage (ou échappement) des données en entrée ou en sortie reste la mesure de sécurité essentielle pour prévenir les attaques XSS

96.	<b>Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?</b>

- CSRF (Cross-Site Request Forgery) est une attaque qui usurpe l'identité d'un utilisateur de confiance et envoie des commandes non désirées sur un site web.

  Pour se protéger des attaques CSRF, il existe la classique solution du token anti-CSRF

97.	<b>Définir l’attaque par force brute et l’attaque par dictionnaire</b>

- Attaque par force brute : C'est une méthode où l'attaquant essaie toutes les combinaisons possibles de mots de passe ou de clés 
 de chiffrement jusqu'à trouver la bonne.

- Attaque par dictionnaire : C'est une technique où l'attaquant utilise une liste précompilée de mots de passe courants ou de phrases 
  fréquemment utilisées pour deviner le mot de passe ou la clé de chiffrement.

98.	<b>Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement</b>

- File Inclusion : Permet à un attaquant d'inclure des fichiers malveillants dans l'application via des chemins de fichiers manipulés, 
  conduisant potentiellement à l'exécution de code ou à l'accès non autorisé à des fichiers sensibles.

- DoS/DDoS : Vise à rendre un service ou une application inaccessible en surchargeant le serveur avec un grand nombre de requêtes ou de trafic.

- Session Hijacking : Permet à un attaquant de voler un jeton de session valide pour se faire passer pour un utilisateur légitime et accéder à ses données ou ses privilèges.

- Clickjacking : Manipule les utilisateurs en les incitant à cliquer sur des éléments invisibles ou déguisés, ce qui peut déclencher des actions non désirées sur une autre page.

- Security Misconfiguration : Résulte d'une mauvaise configuration des systèmes et applications, exposant ainsi des données sensibles ou des fonctionnalités non sécurisées.

- Software Vulnerabilities : Exploite des bugs ou des failles dans des logiciels pour obtenir un accès non autorisé ou exécuter du code malveillant.

99.	<b>A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?</b>

- L'authentification vérifie l'identité d'un utilisateur, assurant qu'il est bien celui qu'il prétend être. 

- L'autorisation détermine les actions et ressources auxquelles cet utilisateur authentifié peut accéder, en fonction de ses permissions.

100. <b>Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage</b>

- Le hachage d'un mot de passe consiste à transformer le mot de passe en une suite de caractères uniques et incompréhensibles. 
  Les algorithmes de hachage courants incluent MD5, SHA-256, et bcrypt.

101. <b>Qu’est-ce qu’une politique de mots de passe forts ?</b>

- Une politique de mots de passe forts est un ensemble de règles qui visent à rendre les mots de passe difficiles à deviner. 
  Ces règles incluent généralement une longueur minimale, l'utilisation de majuscules, de minuscules, de chiffres et de caractères spéciaux, 
  et l'interdiction de mots de passe courants ou simples.

102. <b>Qu’est-ce que l’hameçonnage ?</b>

- L’hameçonnage est une technique utilisée par les pirates pour obtenir des informations sensibles 
  en se faisant passer pour une entité de confiance via des emails, des messages ou des sites web frauduleux.

103. <b>Définir la « validation des entrées »</b>

- C'est le processus de vérification des données que les utilisateurs envoient à un site web ou une application pour s'assurer 
  qu'elles sont correctes et sûres avant de les utiliser ou de les stocker. Cela aide à éviter les erreurs ou les attaques.


## RGPD

104. <b>Qu’est-ce que le RGPD ?</b>

- Le RGPD (Règlement Général sur la Protection des Données) est une réglementation visant à protéger les données personnelles 
  des citoyens de l'UE et à harmoniser les lois sur la protection des données à travers l'Europe.

105. <b>Quel est son objectif principal ?</b>

- L'objectif principal du RGPD est de protéger les données personnelles des citoyens de l'Union Européenne en renforçant leurs droits à la vie privée 
  et en harmonisant les lois sur la protection des données à travers l'Europe.

106. <b>Quelle est la date d’entrée en vigueur du RGPD ?</b>

-  Elle est une réglementation européenne entrée en vigueur depuis le 25 mai 2018

107. <b>Quelles sont les sanctions possibles en cas de non-respect du RGPD ?</b>

- En cas de non-respect du RGPD, les sanctions possibles incluent des amendes pouvant aller jusqu'à 20 millions d'euros 
  ou 4 % du chiffre d'affaires annuel mondial de l'entreprise, le montant le plus élevé étant retenu.

108. <b>En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?</b>

-

109. <b>Quel est le consentement valide selon le RPGD ?</b>

-

110. <b>Qu’est-ce qu’une politique de confidentialité ?</b>

-

111. <b>Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?</b>

-

112. <b>Quels sont les droits des utilisateurs selon le RGPD ?</b>

-

113. <b>Qu’est-ce que le principe de minimisation des données selon le RGPD ?</b>

-


## SEO

114. <b>Qu’est-ce que le SEO ? </b>

-

115. <b>Quel est l’objectif principal du SEO ?</b>

-

116. <b>Existe-t-il plusieurs types de référencement ? Lesquels ?</b>

-

117. <b>Qu’est-ce que la densité de mots-clés en SEO ?</b>

-

118. <b>Qu’est-ce qu’une balise « alt » ?</b>

-

119. <b>Qu’est-ce que la balise « meta description » ?</b>

-

120. <b>Qu’est-ce que le « nofollow » en SEO ?</b>

-

121. <b>Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?</b>

-

122. <b>Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?</b>

-

123. <b>Quelle est la recommandation pour les URL d'un site web bien référencé ?</b>

-

124. <b>Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?</b>

-

125. <b>Qu'est-ce que l'optimisation des images pour le référencement ?</b>

-

126. <b>Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?</b>

-


## Gestion de projets - DevOps

127. <b>Qu’est-ce que la gestion de projet ? </b>

-

128. <b>Qu’est-ce qu’une méthode Agile de gestion de projet ? </b>

-

129. <b>Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages</b>

-

130. <b>A quoi sert la méthodologie MVP ? Citer les caractéristiques clés</b>

-

131. <b>Qu’est-ce que la planification itérative ?</b>

-

132. <b>Citer 3 méthodes Agiles dans le cadre d’un projet informatique</b>

-

133. <b>Qu’est-ce qu’une réunion de revue de projet ?</b>

-

134. <b>Qu’est-ce qu’un livrable dans un projet ? </b>

-

135. <b>Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux</b>

-

136. <b>Qu’est-ce que le DevOps et quel est son objectif principal ?</b>

-

137. <b>Qu’est-ce que l’intégration continue ? </b>

-

138. <b>Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?</b>

-

139. <b>Qu’est-ce qu’un test unitaire ? </b>

-

140. <b>Quelle est l'unité de code testée lors d'un test unitaire ?</b>

-

141. <b>Quelles sont les caractéristiques d'un bon test unitaire ?</b>

-

142. <b>Qu'est-ce qu'une assertion dans un test unitaire ?</b>

-

 
## English

143.	<b> What does JavaScript enable you to do on a website ?</b> 
- a.	Add interactive behavior and dynamic content 
- b.	Define the layout and design of web pages
- c.	Handle server-side operations

// Réponse : <b>A</b>

144.	<b>Which programming language is primarily used for server-side web development ?</b>
- a.	PHP 
- b.	JavaScript
- c.	HTML

// Réponse : <b>A</b>

145.	<b>What is the purpose of a web browser ?</b>
- a.	To render and display web pages
- b.	To execute serve-side code
- c.	To manage databases

// Réponse : <b>A</b>

145.	<b>What is the difference between GET and POST methods in HTTP ?</b>
- a.	GET retrieves data from a server, while POST submits data to a server  
- b.	GET submits data to a server, while POST retrieves data from a server
- c.	GET and POST methods are interchangeable

// Réponse : <b>A</b>

146.	<b>What is the purpose of version control systems (e.g., Git) in web development ?</b>
- a.	To track changes and manage collaborative development 
- b.	To optimize website loading speed
- c.	To handle server-side scripting

// Réponse : <b>A</b>

147.	<b>What is the purpose of a framework in web development ?</b>
- a.	To provide a structured environment for building web applications
- b.	To handle network protocols and data transfer
- c.	To create visual designs and layouts for websites

// Réponse : <b>A</b>

148.	<b>What does NoSQL stand for ?</b>
- a.	Not Only SQL
- b.	Non-Structured Query Language
- c.	New Object-Oriented Language

// Réponse : <b>A</b>

149.	<b>Which of the following is a characteristic of NoSQL databases ?</b> 
- a.	Strict schema enforcement
- b.	Support for complex transactions
- c.	Scalability and flexible data models 

// Réponse : <b>C</b>
