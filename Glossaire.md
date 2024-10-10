GLOSSAIRE / QUIZ
Ce glossaire est prévu pour valider les connaissances après chaque exercice clé de votre formation. L’idée est de réussir à définir les différentes notions en une à 3 phrases maximum et d’adopter le vocabulaire technique approprié. Ce document vous servira comme base de révisions.
A chaque fois qu’un acronyme est cité dans le glossaire, il sera impératif de donner la signification de chaque lettre initiale.

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

1) Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte

- Il est nécessaire d’avoir un environnement serveur doté d’un serveur web Apache qui prend en charge PHP. Parmi les logiciels mettant à disposition un serveur Apache, nous pouvons citer Laragon, WAMP (Windows), MAMP (MacOs) ou LAMP (Linux).

2) Qu’est-ce qu’un algorithme ?

- Un algorithme est une séquence d'instructions (étapes logiques et ordonnées) ou de règles bien définies et non ambiguës (garantissant une meilleure clarté) utilisées pour résoudre un problème ou effectuer une tâche spécifique de manière efficace (en utilisant un minimum de ressources).

3) Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?

- Une variable est un espace de mémoire réservé (caractérisée par un nom) pour stocker une valeur donnée. En PHP, le nom de la variable est préfixé par le symbole $ (dollar). Comme PHP est un langage faiblement typé, le type de données est automatiquement déduit lors de l'assignation de valeur à la variable.

4) Qu’est-ce que la portée d’une variable ?

- La portée d'une variable fait référence à la visibilité et à l'étendue de validité d'une variable dans un programme. Elle détermine les parties du code où la variable peut être utilisée et référencée. La portée peut être locale, limitée à un bloc de code spécifique tel qu'une fonction, ou globale, accessible dans tout le programme.

5) Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?

- Une constante est un élément de programmation dont la valeur ne peut pas être modifiée une fois qu'elle a été définie. Contrairement aux variables, les constantes conservent leur valeur fixe tout au long de l'exécution du programme. En PHP, les constantes sont déclarées à l'aide de la fonction define().

6) Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation

- Une superglobale est une variable prédéfinie dans PHP qui est accessible de partout dans le script, sans avoir besoin de la déclarer ou de l'importer explicitement. Les superglobales sont des tableaux associatifs et sont automatiquement disponibles dans tous les contextes du script PHP, y compris les fonctions, les classes et les fichiers inclus.
-  $_GET : contient les valeurs des paramètres passés via une requête HTTP GET. Par exemple, si l'URL est "http://example.com/page.php?id=123", alors $_GET['id'] contiendra la valeur "123".
-  $_POST : contient les valeurs des paramètres envoyés via une requête HTTP POST. Les données de formulaire envoyées avec la méthode POST sont accessibles à travers cette superglobale.
-  $_SERVER : fournit des informations sur l'environnement du serveur et la requête en Entier (integer) : Les entiers représentent les nombres entiers sans décimales. Par exemple :client, les informations sur le serveur, etc.
-  $_SESSION : permet de stocker et de récupérer des variables de session, qui sont utilisées pour maintenir des données persistantes sur plusieurs pages ou requêtes.
-  $_COOKIE : contient les valeurs des cookies envoyés par le client. Les cookies sont de petites données stockées sur le navigateur du client et sont utilisés pour maintenir des informations entre les différentes requêtes.
- $_FILES : contient des informations sur les fichiers téléchargés via un formulaire d'envoi de fichiers. Il permet d'accéder aux propriétés des fichiers téléchargés, comme le nom du fichier, le type MIME et l'emplacement temporaire du fichier sur le serveur.

7) Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)

- En PHP, il existe plusieurs types de données primitifs que l'on peut associer à une variable. Voici les principaux types de données avec des exemples :

A)  Entier (integer) : les entiers représentent les nombres entiers sans décimales :

- $age = 25;
- $quantite = -10;

B) Nombre à virgule flottante (float) : les nombres à virgule flottante représentent les nombres décimaux :

- $prix = 9.99;
- $pi = 3.14159;

C) Chaîne de caractères (string) : les chaînes de caractères représentent du texte. Elles sont entourées de guillemets simples ('') ou de guillemets doubles ("") :

-  $nom = 'John Doe';
- $message = "Bonjour, comment ça va ?";

D) Booléen (boolean) : les booléens représentent les valeurs de vérité, soit true (vrai) ou false (faux) :

-  $estVrai = true;
-  $estFaux = false;

E) Tableau (array) : les tableaux sont des structures de données permettant de stocker plusieurs valeurs dans une seule variable :

-  $nombres = array(1, 2, 3, 4, 5);
-  $prenom = ['John', 'Jane', 'Alice'];

F) Null : Null est une valeur spéciale qui indique l'absence de valeur :

-  $variableSansValeur = null;
-  Objet (object) : les objets sont utilisés dans la programmation orientée objet (POO) et représentent des instances de classes.

8) Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?

En PHP, il existe plusieurs types de tableaux. Les principaux types de tableaux sont :

• Tableaux indexés : ce sont les tableaux les plus simples où les valeurs sont associées à des indices numériques qui commencent à zéro
o $tableau = ["valeur1", "valeur2", "valeur3"];
• Tableaux associatifs : dans ce type de tableau, les valeurs sont associées à des clés (ou des noms) plutôt qu'à des indices numériques. Chaque valeur est accessible en utilisant sa clé unique correspondante :
o $tableau = ["clé1" => "valeur1", "clé2" => "valeur2", "clé3" => "valeur3"];
• Tableaux multidimensionnels : ce sont des tableaux qui contiennent d'autres tableaux comme valeurs. Ils permettent de représenter des structures de données complexes avec des niveaux imbriqués :
o $tableau = [
["valeur1", "valeur2"],
["valeur3", "valeur4"],
["valeur5", "valeur6"]
];

9) Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ?

En algorithmie, il existe plusieurs structures de contrôle pour gérer le flux d'exécution d'un programme :
• Structure de contrôle conditionnelle (if / else) : permet d'exécuter un bloc de code en fonction d'une condition donnée.
• Structure de contrôle conditionnelle multiple (if / elseif / else) : permet de tester plusieurs conditions successivement et d'exécuter le bloc de code correspondant à la première condition qui est vérifiée.
• Structure de contrôle boucle (for) : permet de répéter un bloc de code un nombre prédéfini de fois.
• Structure de contrôle boucle (while) : Permet de répéter un bloc de code tant qu'une condition donnée est vraie.
• Structure de contrôle boucle avec sortie anticipée (break) : Permet de sortir d'une boucle prématurément si une condition donnée est vérifiée.
• Structure de contrôle boucle avec saut à l'itération suivante (continue) : Permet de passer à l'itération suivante d'une boucle sans exécuter le reste du code pour cette itération.

10) Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?

La fonction PHP qui permet de demander la longueur d'une chaîne de caractères est strlen() (attention, cette fonction compte également les espaces).

11) Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP

En PHP, une session est un mécanisme qui permet de stocker des données côté serveur pour un utilisateur spécifique pendant une période donnée. Une session est créée lorsque l'utilisateur accède à un site web et peut être utilisée pour stocker des informations telles que des préférences utilisateur, des paniers d'achat ou des données de connexion.
La fonction qui permet de démarrer une session en PHP est session_start(). Cette fonction doit être appelée avant d'interagir avec la session pour initialiser ou récupérer les données de session. Ensuite, des données sont stockées dans la variable superglobale $_SESSION.

12) Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP

Un cookie est un petit fichier texte stocké sur l'ordinateur du client (le navigateur) par le serveur web. Les cookies sont utilisés pour stocker des informations spécifiques sur l'utilisateur et peuvent être récupérés par le serveur lors de visites ultérieures.
En PHP, les cookies sont gérés à l'aide de la fonction setcookie(). Cette fonction permet de définir un cookie en spécifiant son nom, sa valeur, sa durée de validité, son chemin, son domaine, etc.
• setcookie('nom', 'John Doe', time() + 3600, '/');

13) Quelle est la différence entre les instructions « require » et « include » en PHP

En PHP, les instructions require et include sont utilisées pour inclure le contenu d'un fichier dans un autre fichier. La principale différence entre les deux réside dans la gestion des erreurs.
L'instruction require est utilisée pour inclure un fichier obligatoire dans un script. Si le fichier spécifié par require n'est pas trouvé ou s'il y a une erreur lors de son inclusion, une erreur fatale se produit, le script est arrêté et un message d'erreur est affiché.
L'instruction include, quant à elle, est utilisée pour inclure un fichier dans un script. Si le fichier spécifié par include n'est pas trouvé ou s'il y a une erreur lors de son inclusion, une simple erreur est affichée, mais le script continue de s'exécuter.
Si le fichier est essentiel, il est recommandé d'utiliser require. Si le fichier est facultatif ou non critique, include peut être utilisé.

14) Comment effectuer une redirection en PHP ?

En PHP, il est possible d'effectuer une redirection vers une autre page en utilisant la fonction header() avec l'en-tête HTTP "Location"
• header('Location: nouvelle_page.php'); exit;
L'instruction exit est utilisée immédiatement après la redirection pour arrêter l'exécution du script et s'assurer que la redirection est effectuée correctement.

15) Définir la partie « front-end » et « back-end » d’une application

Le front-end concerne tout ce qui est visible et interactif pour les utilisateurs (HTML, CSS, JS), tandis que le back-end gère les processus en arrière-plan et les fonctionnalités qui ne sont pas directement accessibles aux utilisateurs (PHP, Python, Ruby, Java, …). Les deux parties travaillent ensemble pour fournir une application complète et fonctionnelle.

16) Définir le contrôle de version ? Qu’est-ce que Git ?

Le contrôle de version est un système qui permet de suivre et de gérer les modifications apportées à un ensemble de fichiers au fil du temps. Il enregistre les différentes versions d'un projet, permet de revenir à des versions antérieures, de fusionner les modifications et de collaborer efficacement entre développeurs.
Git est un exemple de système de contrôle de version décentralisé crée en 2005 par Linus Torvalds (fondateur de Linux).

17) Qu’est-ce qu’un CMS ? Citer au moins 2 exemples

Un CMS (Content Management System) est un système de gestion de contenu qui permet de créer, gérer et organiser facilement le contenu d'un site web. Il offre une interface conviviale pour gérer le contenu sans avoir besoin de connaissances techniques approfondies en programmation.
Wordpress et Joomla sont des exemples de CMS. Ils offrent une grande communauté d'utilisateurs, une documentation étendue et un écosystème de thèmes et de plugins pour étendre les fonctionnalités de base du CMS (autres exemples : Drupal, Magento, Shopify, Wix).

## Front-end

1) Définir HTML

HTML (HyperText Markup Language) est le langage de balisage utilisé pour structurer le contenu des pages web. Il permet de définir la structure logique et les éléments visuels d'une page en utilisant des balises et des attributs spécifiques.

2) Définir CSS

CSS (Cascading Style Sheets) est un langage de style utilisé pour décrire la présentation et l'apparence visuelle d'une page web écrite en HTML. Il permet de contrôler les couleurs, les polices, les marges, les alignements et d'autres aspects de la mise en page pour améliorer l'esthétique et l'expérience utilisateur d'un site web.

3) Définir Javascript

JavaScript est un langage de programmation côté client utilisé pour rendre les pages web interactives et dynamiques. Il permet d'ajouter des fonctionnalités avancées telles que des effets visuels, des validations de formulaire, des requêtes AJAX et la manipulation du contenu HTML et CSS, le tout directement dans le navigateur de l'utilisateur.

4) Définir JSON. Dans quel contexte ce format est-il utilisé ?

JSON (JavaScript Object Notation) est un format de données léger et facile à lire et à écrire (syntaxe simple constituée de paires clé-valeur). Il est utilisé pour représenter et échanger des données structurées entre un serveur et un client, ou entre différentes applications. JSON est largement utilisé dans les services Web, les API (Application Programming Interface) et les échanges de données entre applications.

5) Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?

Oui, il est possible d'interpréter du JavaScript côté serveur grâce à des environnements d'exécution spécifiques. L'un des environnements d'exécution les plus couramment utilisés est Node.js (environnement d'exécution JavaScript côté serveur basé sur le moteur JavaScript V8 de Google Chrome). Grâce à Node.js, JavaScript peut être utilisé de manière polyvalente, à la fois côté client et côté serveur, ce qui permet de partager du code entre les deux environnements et de tirer parti d'une seule langue de programmation pour différents aspects d'une application.
6) Qu’est-ce qu’un sélecteur CSS ?
Un sélecteur CSS est un élément utilisé pour cibler et sélectionner des éléments HTML spécifiques auxquels appliquer des règles de style. Il permet de définir quelles parties du document HTML doivent être stylisées avec les règles CSS correspondantes. Les sélecteurs CSS peuvent être basés sur les attributs, les classes, les identifiants, les types d'éléments ou même la relation entre les éléments.
Page 6 sur 22
7) Quelle balise HTML permet de créer un lien hypertexte ?
La balise HTML qui permet de créer un lien hypertexte est la balise <a> (anchor = encre). La balise <a> est utilisée pour définir un lien vers une autre page, un fichier, une section de la même page ou une ressource externe sur Internet.
• <a href="http://www.example.com">Cliquez ici pour visiter le site</a>
8) Qu’est-ce qu’une requête AJAX ?
Une requête AJAX (Asynchronous JavaScript And XML) est une méthode permettant d'échanger des données avec un serveur web en arrière-plan, sans recharger entièrement la page. Elle offre une expérience utilisateur plus interactive et réactive en permettant des mises à jour dynamiques du contenu de la page. Grâce à AJAX, les requêtes peuvent être effectuées de manière asynchrone, ce qui améliore les performances et l'efficacité des applications web.
9) Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
Pour sélectionner tous les éléments d'une classe spécifique, on utilise le sélecteur CSS de classe qui est représenté par le préfixe "." suivi du nom de la classe. Par exemple, pour sélectionner tous les éléments ayant la classe "ma-classe", on utilise le sélecteur CSS ".ma-classe".
Pour sélectionner un élément par son identifiant spécifique, on utilise le sélecteur CSS d'identifiant qui est représenté par le préfixe "#" suivi de l'identifiant. Par exemple, pour sélectionner l'élément avec l'identifiant "mon-id", on utilise le sélecteur CSS "#mon-id".
10) Définir le responsive design
Le responsive design est une approche de conception de sites web qui vise à créer des expériences utilisateur optimales sur différents appareils et tailles d'écran. Il consiste à adapter dynamiquement la mise en page, les images et les éléments interactifs pour offrir une navigation fluide et une lisibilité optimale, quel que soit le dispositif utilisé par l'utilisateur.
11) Qu’est-ce que le templating ?
Le templating est une technique de développement web qui consiste à séparer la structure de la présentation d'une page web. Il permet de réutiliser des modèles prédéfinis pour générer dynamiquement des pages avec du contenu spécifique provenant de différentes sources de données. En utilisant des templates, le développement et la maintenance des sites web deviennent plus efficaces et flexibles, offrant une meilleure séparation des préoccupations et une réutilisation du code.
12) Qu’est-ce qu’une fonction anonyme en Javascript ?
Une fonction anonyme en JavaScript est une fonction sans nom définie de manière inline. Elle peut être assignée à une variable ou utilisée comme une expression de fonction. Les fonctions anonymes sont souvent utilisées dans les callbacks ou les événements en JavaScript.
• var maFonction = function() { … }
13) Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
La méthode JavaScript utilisée pour ajouter un élément à la fin d'un tableau est push(). La méthode push() permet d'ajouter un ou plusieurs éléments à la fin d'un tableau existant et retourne la nouvelle longueur du tableau.
Page 7 sur 22
14) Qu’est-ce qu’un « media query » ?
Un media query est une fonctionnalité du CSS qui permet de définir des règles de style conditionnelles en fonction des caractéristiques du dispositif utilisé pour afficher une page web dans le contexte du responsive design. Il permet d'adapter dynamiquement la mise en page et les styles en fonction des propriétés du média, telles que la taille de l'écran, l'orientation, la résolution, etc.
15) Qu’est-ce qu’un pseudo élément en CSS ?
Un pseudo-élément en CSS est un élément virtuel qui permet de sélectionner et de styler une partie spécifique d'un élément HTML. Il permet d'ajouter du contenu ou de modifier l'apparence d'une partie spécifique d'un élément sans avoir à modifier la structure du HTML.
Les pseudo-éléments sont représentés par le double deux-points (::) et sont utilisés avec les sélecteurs CSS. Ils permettent de cibler des parties spécifiques d'un élément, telles que le premier caractère (::first-letter), la première ligne (::first-line), les éléments avant (::before) et après (::after) l'élément, etc.
16) Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
Bootstrap est un framework front-end populaire développé par Twitter. Il s'agit d'une collection de styles prédéfinis, de composants interactifs et de scripts JavaScript qui facilitent la création d'interfaces web réactives et attrayantes. Bootstrap utilise un système de grille flexible, des classes prédéfinies et des composants réutilisables pour accélérer le développement web.
Autres exemples : Tailwind CSS, UiKit, Semantic UI, Materialize CSS, …
17) Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes
Lorsqu'un formulaire HTML est créé, il peut être associé à deux méthodes différentes : GET et POST.
La méthode GET est utilisée pour les opérations de lecture et les données sont ajoutées à l'URL, tandis que la méthode POST est utilisée pour les opérations de création, de modification ou de suppression et les données sont envoyées dans le corps de la requête HTTP.

## UX / UI

1) Quelle est la différence entre UX Design et UI Design ?
L'UX design (User Experience design) se concentre sur l'expérience globale de l'utilisateur lors de l'interaction avec un produit ou un service, en se basant sur des recherches, des tests utilisateurs et des considérations d'utilisabilité.
L'UI design (User Interface design), quant à lui, se concentre sur la conception visuelle et fonctionnelle des interfaces utilisateur, en créant des éléments visuels tels que les boutons, les icônes et les mises en page pour améliorer l'expérience utilisateur.
2) Qu’est-ce qu’un wireframe ?
Un wireframe est une représentation visuelle simplifiée d'une interface utilisateur ou d'une page web, utilisée pour planifier la structure et la disposition des éléments. Il permet de définir les fonctionnalités et les interactions de base sans se préoccuper des détails visuels.
3) Qu’est-ce qu’un prototype ?
Un prototype est une représentation fonctionnelle et interactive d'un produit ou d'une interface utilisateur permettant de tester et d'évaluer son fonctionnement avant le développement complet.
Page 8 sur 22
4) Qu’est-ce que la hiérarchie visuelle en UI Design ?
La hiérarchie visuelle en UI Design se réfère à l'organisation et à la présentation des éléments visuels dans une interface utilisateur de manière à créer une structure claire et compréhensible, où les éléments les plus importants sont mis en évidence et les relations entre eux sont facilement perceptibles par les utilisateurs.
5) Qu’est-ce que l’accessibilité en UX Design ?
L'accessibilité en UX Design se réfère à la conception et à la création de produits numériques ou d'interfaces utilisateur de manière à ce qu'ils puissent être utilisés de façon efficace et conviviale par un large éventail de personnes, y compris celles ayant des capacités physiques, sensorielles ou cognitives réduites. L'objectif de l'accessibilité est de garantir une expérience inclusive pour tous les utilisateurs, en offrant des fonctionnalités et des aides adaptées aux besoins individuels.
6) Qu’est-ce qu’une grille de mise en page ?
Une grille de mise en page est une structure visuelle composée de lignes horizontales et verticales qui délimite et organise l'espace d'une interface utilisateur ou d'une page web. Elle est utilisée pour aligner et positionner les éléments de manière cohérente, facilitant ainsi la création d'une présentation équilibrée, harmonieuse et structurée.
7) Qu’est-ce que la notion d’affordance en UX Design ?
La notion d'affordance en UX Design se réfère à la perception ou à la suggestion d'une action possible ou d'une fonctionnalité d'un objet ou d'une interface utilisateur basée sur ses caractéristiques visuelles ou physiques. Il s'agit de créer des indices ou des signaux visuels qui invitent intuitivement les utilisateurs à interagir avec un élément spécifique de manière appropriée.
Par exemple, un bouton avec une apparence en relief suggère qu'il peut être pressé, offrant ainsi une affordance pour l'action de cliquer.
8) Qu’est-ce qu’un « mobile first design » ?
Le "mobile first design" est une approche de conception qui consiste à concevoir d'abord pour les appareils mobiles avant les autres dispositifs. Cela garantit une expérience utilisateur optimale sur les écrans mobiles tout en offrant une adaptation progressive vers des écrans plus grands.

## Programmation orientée objet (POO)

1) Donner une définition de la programmation orientée objet
La programmation orientée objet (POO) est un paradigme de programmation qui organise le code autour de concepts de classes, d’objets et d’instances plutôt que de simples instructions.
2) Qu’est-ce qu’une classe ? Comment la déclare-t-on en PHP ?
Une classe en programmation orientée objet est un modèle ou un plan qui définit les attributs et les méthodes communes à un groupe d'objets. Elle sert de structure pour créer des instances d'objets avec des caractéristiques similaires.
En PHP :
• class MaClasse { // Définition des attributs et des méthodes de la classe }
Page 9 sur 22
3) Qu’est-ce qu’un objet ?
Les objets en programmation orientée objet sont des instances de classes qui regroupent des données (attributs) et des fonctionnalités (méthodes) liées. Les objets sont des entités virtuelles qui représentent des concepts ou des éléments du monde réel dans le contexte de la programmation.
En PHP, un objet est une instance spécifique d'une classe. Il est créé en utilisant le mot-clé new suivi du nom de la classe, suivi éventuellement de parenthèses contenant les arguments du constructeur si la classe en possède un.
4) Définir la notion de propriété / attribut / méthode
Les propriétés sont les variables qui contiennent les données de l'objet, tandis que les méthodes sont les fonctions qui définissent les actions que l'objet peut effectuer et les opérations qu'il peut exécuter. Les propriétés décrivent l'état de l'objet, tandis que les méthodes définissent son comportement.
5) Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité
La visibilité d'une propriété ou d'une méthode en programmation orientée objet définit l'accès et la portée de ces éléments à l'intérieur d'une classe. Elle détermine si ces éléments peuvent être accessibles à partir d'autres parties du code.
Les différents types de visibilité couramment utilisés sont :
• Public : les propriétés et les méthodes publiques sont accessibles à partir de n'importe quelle partie du code, y compris à l'extérieur de la classe.
• Protected : les propriétés et les méthodes protégées sont accessibles uniquement à l'intérieur de la classe qui les déclare, ainsi que par les classes dérivées (classes enfants) qui héritent de cette classe.
• Private : les propriétés et les méthodes privées sont accessibles uniquement à l'intérieur de la classe qui les déclare. Elles ne sont pas visibles par les classes dérivées ou par d'autres parties du code.
La visibilité permet de contrôler l'accès aux éléments d'une classe, ce qui contribue à encapsuler et à protéger les données et le comportement de l'objet.
6) Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
La méthode spécifique utilisée pour créer un nouvel objet à partir d'une classe en PHP est le constructeur de classe. Le constructeur est une méthode spéciale dans une classe qui est automatiquement appelée lors de la création d'un nouvel objet à partir de cette classe.
7) Qu’est-ce que l’encapsulation ?
L'encapsulation se réfère à la capacité d'un objet à regrouper ses données (attributs) et ses méthodes associées, en les maintenant privées ou protégées, et en fournissant des méthodes publiques pour interagir avec ces données. Cela permet de cacher les détails internes de l'objet et de contrôler l'accès et la manipulation de ses données. L'encapsulation permet également de définir des règles et des validations pour garantir l'intégrité et la cohérence des données de l'objet.
8) Que signifie « étendre une classe » ? Quelle est le concept clé mis en oeuvre ? Donner un exemple
Lorsqu'on parle d'étendre une classe en programmation orientée objet, cela signifie créer une nouvelle classe (appelée classe dérivée ou sous-classe) qui hérite des caractéristiques (propriétés et méthodes) d'une classe existante (appelée classe de base ou superclasse). Le concept clé mis en oeuvre est l'héritage.
• class Vehicule (classe parent)
• class Voiture extends Vehicule (classe dérivée / sous-classe)
• parent::__construct($attribut);
Page 10 sur 22
9) Définir l’opérateur de résolution de portée
L'opérateur de résolution de portée (->) est utilisé en programmation pour accéder aux membres d'un objet à partir d'une instance de classe.
Il permet de spécifier le contexte dans lequel une propriété ou une méthode est recherchée et utilisée. En utilisant cet opérateur, on peut accéder aux propriétés et méthodes spécifiques d'un objet, ce qui facilite la manipulation des données et l'exécution des actions associées à cet objet.
10) Définir une méthode / propriété statique
Une méthode ou une propriété statique en programmation est associée à la classe elle-même plutôt qu'à une instance particulière de cette classe. Une méthode statique est déclarée avec le mot-clé static et peut être appelée directement à partir de la classe sans instanciation préalable. Une propriété statique est une variable de classe partagée par toutes les instances de cette classe. Les méthodes et propriétés statiques sont souvent utilisées pour des fonctionnalités ou des valeurs communes à toutes les instances de la classe, ou pour des opérations qui ne nécessitent pas l'état spécifique d'un objet.
11) Définir le polymorphisme en POO
Le polymorphisme en POO permet à des objets de différentes classes d'implémenter une même méthode avec des comportements spécifiques à chaque classe. Cela facilite la gestion et la réutilisation du code pour des objets ayant un comportement commun.
12) Définir une méthode / classe abstraite ?
Une classe abstraite est une classe qui ne peut pas être instanciée directement. Elle sert de classe de base pour d'autres classes dérivées, et peut contenir des méthodes abstraites ainsi que des méthodes concrètes. Les classes dérivées doivent implémenter les méthodes abstraites définies dans la classe abstraite, tout en pouvant étendre son comportement en ajoutant de nouvelles méthodes ou en redéfinissant les méthodes existantes.
13) Définir le chaînage de méthodes
Le chaînage de méthodes, également connu sous le nom de "chaining" en anglais, est une technique qui permet d'appeler plusieurs méthodes successivement sur un même objet, en les enchaînant les unes après les autres, sans avoir besoin d'affecter le résultat intermédiaire à une variable séparée.
• $voiture = new Voiture();
• $voiture->setMarque("Toyota")->setModele("Camry")->setAnnee(2022)->afficherDetails();
14) Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques »
La méthode magique __toString() est une méthode spéciale en PHP qui permet de définir le comportement d'un objet lorsqu'il est converti en une chaîne de caractères. Lorsqu'un objet est utilisé dans un contexte où une chaîne de caractères est attendue, la méthode __toString() est automatiquement appelée et son résultat est retourné.
Il existe d’autres méthodes « magiques » comme : __construct, __get et __set, __isset et __unset, __destruct, etc. (__destruct ne doit pas être appelée manuellement, car elle est automatiquement invoquée par le gestionnaire de mémoire de PHP lorsque l'objet n'est plus utilisé).
Page 11 sur 22
15) Qu’est-ce qu’un « autoload » ?
L'autoload est un mécanisme en PHP permettant de charger automatiquement les classes lors de leur utilisation sans avoir à les inclure manuellement. Il évite d'avoir à gérer manuellement les inclusions de fichiers pour chaque classe utilisée. En utilisant une fonction d'autoload personnalisée ou spl_autoload_register(), les fichiers correspondants aux classes sont chargés automatiquement lorsque nécessaire, simplifiant ainsi le développement et la gestion des dépendances.
16) Comment appelle-t-on en français les « getters » et les « setters » ?
En français, les "getters" sont souvent appelés "accesseurs" et les "setters" sont appelés "mutateurs". Les accesseurs sont des méthodes qui permettent de récupérer la valeur d'une propriété d'un objet, tandis que les mutateurs sont des méthodes qui permettent de modifier la valeur d'une propriété d'un objet.
17) Qu’est-ce que la sérialisation en PHP ?
La sérialisation en PHP est le processus de conversion d'un objet en une représentation linéaire qui peut être stockée ou transmise, par exemple, en tant que chaîne de caractères ou fichier. Cela permet de sauvegarder l'état de l'objet et de le restaurer ultérieurement, tout en préservant sa structure et ses données.

## Architecture

1) Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence
L'architecture client/serveur est un modèle où un client et un serveur travaillent ensemble pour fournir des services. Le client envoie des requêtes au serveur, qui les traite et renvoie les réponses correspondantes. Pour interroger le serveur, le client utilise généralement des requêtes HTTP, qui permettent d'envoyer des demandes et de recevoir des réponses. L'acronyme "HTTP" (HyperText Transfer Protocol) représente le protocole utilisé pour ces requêtes. Lorsque le "S" est ajouté pour former "HTTPS", cela indique que la communication est sécurisée grâce à une couche de chiffrement.
2) Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
Un design pattern, ou motif / patron de conception, est une solution réutilisable à un problème courant de conception de logiciel. Il fournit des directives et des bonnes pratiques pour structurer et organiser le code de manière efficace et maintenable. Parmi les nombreux design patterns existants, nous pouvons citer : MVC (model, view, controller), Singleton (permet de s'assurer qu'une classe ne possède qu'une seule instance dans tout le programme), Observer (permet de mettre en place une communication de type "publier/souscrire" entre des objets, où un objet appelé "sujet" informe automatiquement ses "observateurs" de tout changement d'état), Factory (permet de créer des objets sans spécifier explicitement leur classe, en utilisant une méthode de fabrication dédiée), Composite, Adapter, Strategy, Facade, Iterator, Decorator, etc.
3) Qu’est-ce que l’architecture MVC ?
L'architecture MVC (Modèle-Vue-Contrôleur) est un pattern de conception utilisé pour organiser la structure d'une application logicielle. Elle divise l'application en trois composants principaux : Model, View et Controller.
Page 12 sur 22
4) Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
• Le Modèle représente les données et la logique métier de l'application. Il gère la manipulation, la récupération et la mise à jour des données.
• La Vue est responsable de l'interface utilisateur. Elle affiche les données au format approprié et permet à l'utilisateur d'interagir avec l'application.
• Le Contrôleur gère la logique de traitement des requêtes de l'utilisateur. Il reçoit les actions de l'utilisateur depuis la Vue, interagit avec le Modèle pour obtenir les données nécessaires, puis met à jour la Vue en conséquence.
5) Quels sont les avantages de l’architecture MVC ?
L'architecture MVC présente les avantages suivants : séparation claire des préoccupations, réutilisabilité du code, testabilité, évolutivité et collaboration efficace.
6) Existe-t-il des variantes à l’architecture MVC ?
• Modèle-Vue-Présentation (MVP) : Dans cette variante, le Présentateur (ou le Présentation Model) prend en charge le rôle du Contrôleur, tandis que la Vue est passivement mise à jour par le Présentateur.
• Modèle-Vue-VueModèle (MVVM) : Cette variante introduit un composant supplémentaire appelé VueModèle, qui se situe entre le Modèle et la Vue. Le VueModèle gère la logique de présentation et fournit des données spécifiquement formatées pour la Vue.
7) Qu’est-ce qu’une API ? Définir l’architecture REST
Une API (Interface de programmation d'application) est une interface permettant à différentes applications de communiquer entre elles en suivant des règles et des protocoles. L'architecture REST (Representational State Transfer) est un style d'architecture couramment utilisé pour concevoir des services web et des API, en se basant sur le protocole HTTP et les méthodes standardisées. Elle favorise l'interopérabilité et la manipulation des ressources via des méthodes telles que GET, POST, PUT et DELETE.
Modélisation / Base de données
1) Qu’est-ce que la modélisation de données ? Définir la méthode Merise
La modélisation de données est le processus de création d'une représentation structurée des données d'un système, en utilisant des concepts et des notations spécifiques.
La méthode Merise est une méthode de modélisation de données largement utilisée en génie logiciel. Elle utilise des diagrammes entité-association (E/A) pour représenter les entités, les relations et les attributs d'un système.
2) Quelles sont les 3 étapes principales de la méthode Merise ?
a. Analyse, conception et réalisation
b. Planification, exécution et contrôle
c. Création, modification et suppression
3) Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
Un modèle conceptuel de données (MCD) en Merise est une représentation abstraite des entités, relations et attributs d'un système d'information. Il offre une vision globale et simplifiée de la structure des données sans tenir compte des détails techniques. Le MCD est utilisé comme base pour développer les modèles logique et physique de données dans le processus de modélisation Merise.
Page 13 sur 22
4) Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
Le modèle logique de données (MLD) en Merise est une représentation détaillée du modèle conceptuel de données (MCD) qui traduit les entités, relations et attributs en structures spécifiques au système de gestion de base de données. Il définit la structure des tables et les relations entre elles, en incluant les clés primaires et étrangères, afin de garantir l'intégrité et la cohérence des données.
5) Donner la définition des mots suivants :
a. Entité : représente un objet ou une chose du monde réel, identifiable et ayant des caractéristiques propres. Elle est généralement représentée par une table dans une base de données, où chaque ligne représente une occurrence unique de cette entité.
b. Relation : est une association entre deux entités dans un modèle de données. Elle représente une connexion sémantique ou une interaction entre les entités. Les relations sont généralement représentées par des liens ou des jointures entre les tables d'une base de données.
c. Cardinalité : indique le nombre d'occurrences d'une entité qui peuvent être associées à une occurrence d'une autre entité via une relation. Elle peut être exprimée en termes de "un à un", "un à plusieurs" ou "plusieurs à plusieurs", indiquant ainsi les contraintes de quantité entre les entités liées.
d. Clé primaire / clé étrangère :
i. Clé primaire est un attribut ou un ensemble d'attributs qui identifie de manière unique chaque occurrence d'une entité dans une table. Elle garantit l'unicité des enregistrements et sert de référence pour établir des relations avec d'autres tables.
ii. Clé étrangère, quant à elle, est un attribut ou un ensemble d'attributs d'une table qui fait référence à la clé primaire d'une autre table, établissant ainsi une relation entre les deux tables. Elle permet de maintenir l'intégrité référentielle et d'établir des liens entre les données.
6) Que devient une relation de type « Many To Many » dans le modèle logique de données ?
Dans le modèle logique de données, une relation de type "Many-to-Many" est généralement résolue en utilisant une table intermédiaire, également appelée table de jonction ou table associative. Cette table associative contient les clés primaires des entités liées, permettant ainsi de représenter les associations multiples entre les entités.
7) Qu’est-ce qu’une base de données ?
Une base de données est un ensemble organisé et structuré de données géré et interrogé pour répondre aux besoins d'une application ou d'un système.
8) Définir les notions suivantes :
a. SQL : (Structured Query Language) est un langage utilisé pour communiquer avec les systèmes de gestion de bases de données relationnelles (SGBDR). Il permet de créer, modifier et interroger des bases de données en utilisant des instructions pour manipuler les données.
b. MySQL est un système de gestion de base de données relationnelle (SGBDR) populaire, largement utilisé pour stocker et gérer des données. Il prend en charge le langage SQL et offre une grande fiabilité, performance et flexibilité, ce qui en fait un choix courant pour de nombreux types d'applications.
c. SGBD (Système de Gestion de Base de Données) : est un logiciel qui permet de créer, manipuler et gérer des bases de données. Exemple : PostgreSQL, SQL Server, Oracle, …
Page 14 sur 22
9) Dans une base de données, les données sont stockées dans des tables. Celles-ci sont constituées de lignes appelées enregistrements (ou entrées) et de colonnes appelées champs.
10) Quelle est la différence entre une base de données relationnelle et non relationnelle ?
Les bases de données relationnelles utilisent des tables structurées avec des relations entre elles, tandis que les bases de données non relationnelles utilisent des modèles de données plus flexibles adaptés aux données non structurées. La différence réside dans la façon dont les données sont organisées et stockées, offrant des approches différentes pour la manipulation et la gestion des données.
11) Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
Une jointure dans une base de données est une opération qui combine les enregistrements de deux ou plusieurs tables en fonction d'une condition de correspondance. Il existe plusieurs types de jointures, notamment la jointure interne, la jointure externe (gauche, droite, complète), la jointure croisée (ou produit cartésien) et la jointure auto-join. Chaque type de jointure a sa propre utilité en fonction des besoins de récupération des données et des relations entre les tables.
En SQL : JOIN, INNER JOIN, LEFT / RIGHT JOIN, FULL JOIN, CROSS JOIN et SELF JOIN
12) A quoi sert une vue dans une base de données ?
Une vue dans une base de données est une représentation virtuelle de données provenant de différentes tables. Elle simplifie l'accès et la manipulation des données en offrant une couche d'abstraction supplémentaire.
13) Qu’est-ce que l’intégrité référentielle dans une base de données ?
L'intégrité référentielle assure que les clés étrangères d'une table font référence à des valeurs valides dans la table parente, garantissant ainsi la cohérence des relations. Elle prévient les références brisées et maintient l'intégrité des données dans la base de données.
14) Quelles sont les fonctions d’agrégation en SQL ?
Les fonctions d'agrégation en SQL permettent de calculer des valeurs agrégées à partir d'un ensemble de données. Parmi les fonctions d'agrégation courantes, on retrouve SUM (pour la somme), AVG (pour la moyenne), COUNT (pour le décompte), MAX (pour la valeur maximale) et MIN (pour la valeur minimale).
15) Qu’est ce qu’un CRUD dans le contexte d’une base de données ?
Dans le contexte d'une base de données, CRUD est un acronyme qui représente les opérations de base réalisées sur les données : Create (Création), Read (Lecture), Update (Mise à jour) et Delete (Suppression).
16) Quelles sont les clauses qui permettent de :
a. Insérer un nouvel enregistrement dans une table : INSERT INTO … VALUES
b. Modifier un enregistrement dans une table : UPDATE … SET
c. Supprimer un enregistrement dans une table : DELETE FROM
d. Supprimer la base de données : DROP DATABASE
e. Filtrer les résultats d’une requête SQL : WHERE
f. Trier les résultats d’une requête SELECT : ORDER BY
g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique : GROUP BY
h. Concaténer 2 chaînes de caractères : CONCAT
Page 15 sur 22
17) Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?
Pour se connecter à une base de données en PHP, on utilise la classe native appelée PDO (PHP Data Objects)
• $pdo = new PDO("mysql:host=$host;dbname=$dbname", $username, $password);

## Symfony

1) Qu’est-ce que Symfony ?
Symfony est un framework open-source et hautement extensible, utilisé pour développer des applications web et des API. Il fournit une large gamme de fonctionnalités prêtes à l'emploi, telles que la gestion des routes, la gestion des formulaires, l'accès aux bases de données, la sécurité, etc., facilitant ainsi le processus de développement.
2) Sur quel langage de programmation et design pattern repose Symfony ?
C’est un framework PHP. Il suit l'architecture MVC (Modèle-Vue-Contrôleur)
3) Quelle est la dernière version en date de Symfony ?
6.3.0 (juin 2023)
4) Qu’est-ce qu’un bundle ?
Un bundle est un composant réutilisable et autonome dans le framework Symfony, regroupant des fonctionnalités spécifiques
5) Quel est le moteur de template utilisé par défaut dans Symfony ?
Le moteur de template utilisé par défaut dans Symfony est Twig. Twig est un moteur de template moderne, puissant et flexible qui facilite la gestion et la manipulation des vues dans les applications Symfony. Il offre une syntaxe intuitive et des fonctionnalités avancées pour rendre le processus de création et de rendu des vues plus efficace et plus sécurisé.
6) Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
Un ORM (Object-Relational Mapping) est un outil qui permet de faire le lien entre les objets de la programmation orientée objet et les tables d'une base de données relationnelle. Son utilité est de simplifier et d'automatiser les opérations de mapping, de persistance et de récupération des données. Dans Symfony, l'ORM utilisé s'appelle Doctrine, qui offre une interface intuitive pour interagir avec la base de données en utilisant des entités PHP plutôt que des requêtes SQL directes.
7) Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?
L'injection de dépendances est un principe de la programmation qui consiste à fournir les dépendances nécessaires à une classe plutôt que de les instancier à l'intérieur de celle-ci. Composer est l'outil utilisé pour la gestion des dépendances. Le fichier "composer.json" contient la liste des dépendances du projet et permet de les installer, de les mettre à jour et de gérer leur version.
8) Que permet le bundle Maker au sein de Symfony ?
Le bundle Maker de Symfony est un outil puissant qui permet aux développeurs de générer rapidement du code boilerplate (code de base) pour différentes parties de leur application. Il simplifie la création de classes d'entités, de contrôleurs, de formulaires et d'autres éléments couramment utilisés.
Page 16 sur 22
9) Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
Symfony propose un langage de requête spécifique appelé DQL (Doctrine Query Language) qui est une variante orientée objet du langage SQL. DQL est utilisé en conjonction avec Doctrine, l'ORM de Symfony, pour effectuer des requêtes et manipuler les objets persistants dans la base de données. Il offre une syntaxe plus orientée objet et abstraite par rapport au SQL pur, facilitant le mapping des objets avec les tables de la base de données.
10) Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?
Le composant de sécurité (Security) de Symfony est responsable de la gestion de l'authentification et de l'autorisation des utilisateurs. Il fournit des fonctionnalités telles que l'authentification basée sur différents mécanismes (par exemple, formulaire de connexion, authentification basée sur un jeton, authentification à l'aide de services tiers, etc.), la gestion des rôles et des permissions, ainsi que des fonctionnalités de contrôle d'accès pour restreindre l'accès aux différentes parties de l'application en fonction des droits des utilisateurs.

## Sécurité

1) Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
L'injection SQL est une technique d'attaque où des données non fiables sont insérées dans une requête SQL, compromettant ainsi la sécurité et l'intégrité des données. Pour prévenir l'injection SQL, il est recommandé d'utiliser des requêtes préparées avec des paramètres liés et de filtrer et valider soigneusement les entrées utilisateur.
2) Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
La faille XSS (Cross-Site Scripting) est une vulnérabilité qui permet à des attaquants d'injecter du code malveillant dans des pages web, ce qui peut entraîner l'exécution de scripts non désirés chez les utilisateurs. Pour se prémunir contre les attaques XSS, il est essentiel de valider et d'échapper correctement toutes les données entrantes et de mettre en oeuvre des mesures de sécurité telles que l'utilisation de filtres de sécurité.
3) Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
La faille CSRF (Cross-Site Request Forgery) est une attaque qui permet à un attaquant de forcer un utilisateur authentifié à effectuer des actions indésirables sans son consentement. Pour se prémunir contre les attaques CSRF, il est recommandé de mettre en place des mécanismes de protection tels que l'utilisation de jetons CSRF (CSRF tokens) dans les formulaires et la vérification de l'origine des requêtes (Origin header) côté serveur.
4) Définir l’attaque par force brute et l’attaque par dictionnaire
L'attaque par force brute est une méthode d'attaque où l'attaquant essaie toutes les combinaisons possibles de mots de passe ou de clés jusqu'à trouver la bonne.
L'attaque par dictionnaire est une méthode d'attaque similaire où l'attaquant utilise une liste prédéfinie de mots de passe ou de clés couramment utilisés pour tenter de trouver l'accès.
5) Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
Les attaques par déni de service (DoS) : Ces attaques visent à rendre un service indisponible en surchargeant les ressources du serveur, ce qui entraîne l'incapacité des utilisateurs légitimes à accéder au service.
L'usurpation d'identité (phishing) : Cette attaque consiste à tromper les utilisateurs en se faisant passer pour une entité de confiance afin de leur soutirer des informations sensibles telles que des mots de passe ou des informations de carte de crédit.
Page 17 sur 22
6) A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
En combinant l'authentification et l'autorisation, les applications web peuvent garantir que seuls les utilisateurs autorisés ont accès aux fonctionnalités appropriées et aux données sensibles, renforçant ainsi la sécurité et la confidentialité des informations.
7) Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
Le hachage d'un mot de passe est le processus de conversion d'un mot de passe en une chaîne de caractères alphanumériques de longueur fixe, appelée "hash" ou "empreinte". Ce processus est irréversible, ce qui signifie qu'il est difficile, voire impossible, de retrouver le mot de passe d'origine à partir du hash. Les algorithmes de hachage couramment utilisés incluent Argon2i et BCrypt par exemple.
8) Qu’est-ce qu’une politique de mots de passe forts ?
Une politique de mots de passe forts vise à établir des critères stricts pour la création de mots de passe sécurisés. Cela peut inclure des exigences telles que des longueurs minimales, l'utilisation de caractères variés et l'exclusion de mots courants. L'objectif est de renforcer la sécurité des comptes en réduisant les risques d'attaques par force brute ou de compromission des mots de passe.
9) Qu’est-ce que l’hameçonnage ? (voir question 5 -> phishing)
10) Définir la « validation des entrées »
La validation des entrées consiste à vérifier la conformité des données saisies par les utilisateurs selon des critères prédéfinis tels que le format, la longueur et la validité. Elle est essentielle pour prévenir les erreurs et les attaques potentielles liées à des données malveillantes ou incorrectes.

## RGPD

1) Qu’est-ce que le RGPD ?
Le RGPD est le Règlement Général sur la Protection des Données
2) Quel est son objectif principal ?
L'objectif principal du RGPD est de renforcer la protection des données personnelles des individus en établissant des règles claires et strictes pour leur collecte, leur utilisation et leur conservation. Il vise également à responsabiliser les organisations dans la gestion des données et à garantir les droits des individus sur leurs propres informations personnelles.
3) Quelle est la date d’entrée en vigueur du RGPD ?
Le RGPD est entré en vigueur le 25 mai 2018.
4) Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
En cas de non-respect du RGPD, des sanctions financières peuvent être imposées aux organisations jusqu'à 20 millions d'euros ou 4 % du chiffre d'affaires mondial annuel, selon le montant le plus élevé. Les autorités de protection des données ont également le pouvoir d'ordonner des mesures correctives, de suspendre ou de limiter le traitement des données, voire de procéder à des interdictions complètes d'activités de traitement. Les personnes concernées par une violation du RGPD ont également le droit d'intenter des actions en justice pour obtenir réparation.
Page 18 sur 22
5) En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
En France, c'est la Commission Nationale de l'Informatique et des Libertés (CNIL) qui est l'autorité administrative chargée de faire appliquer le RGPD.
6) Quel est le consentement valide selon le RPGD ?
Selon le RGPD, le consentement valide doit être donné de manière libre, éclairée, spécifique et univoque par la personne concernée. Il doit être obtenu par une action positive claire et affirmative, et il doit être révocable à tout moment. Le consentement doit également être basé sur des informations claires et compréhensibles sur le traitement des données et ses finalités.
7) Qu’est-ce qu’une politique de confidentialité ?
Une politique de confidentialité est un document qui informe les utilisateurs sur la manière dont leurs données personnelles sont collectées, utilisées, partagées et protégées par une entreprise ou une organisation. Elle définit les droits et les choix des utilisateurs en matière de confidentialité et explique les mesures prises pour garantir la sécurité des données.
8) Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
Selon le RGPD, la durée de conservation des données personnelles doit être limitée et proportionnée à la finalité pour laquelle elles ont été collectées. En général, les données personnelles ne doivent pas être conservées plus longtemps que nécessaire pour atteindre l'objectif spécifique pour lequel elles ont été traitées. Cependant, il n'y a pas de durée de conservation maximale spécifique définie par le RGPD, car celle-ci peut varier en fonction du contexte et des exigences légales ou réglementaires applicables.
9) Quels sont les droits des utilisateurs selon le RGPD ?
Selon le RGPD, les utilisateurs disposent de certains droits en ce qui concerne leurs données personnelles. Ils ont le droit d'être informés de la collecte et de l'utilisation de leurs données, d'accéder à leurs données personnelles, de demander leur rectification ou leur effacement, de limiter le traitement de leurs données, de s'opposer au traitement et d'exercer leur droit à la portabilité des données.
10) Qu’est-ce que le principe de minimisation des données selon le RGPD ?
Le principe de minimisation des données du RGPD vise à limiter la collecte et le traitement des données personnelles aux seules informations nécessaires pour atteindre les objectifs spécifiques. Il implique de ne pas conserver les données plus longtemps que nécessaire et de s'assurer que seules les données pertinentes sont collectées.

## SEO

1) Qu’est-ce que le SEO ?
Le SEO (Search Engine Optimization) est l’acronyme anglophone pour le référencement.
2) Quel est l’objectif principal du SEO ?
L'objectif principal du SEO est d'augmenter la visibilité d'un site web dans les résultats de recherche afin d'attirer un trafic organique de qualité et d'améliorer sa visibilité en ligne, ce qui peut se traduire par une augmentation du nombre de visiteurs, de conversions et de notoriété de la marque.
Page 19 sur 22
3) Existe-t-il plusieurs types de référencement ? Lesquels ?
Le référencement naturel (SEO) vise à optimiser le positionnement d'un site web dans les résultats de recherche organiques.
Le référencement payant (SEA) consiste à acheter des annonces publicitaires pour apparaître en tête des résultats sponsorisés.
Le référencement social (SMO) concerne l'optimisation de la présence d'un site web sur les réseaux sociaux pour générer du trafic et augmenter la visibilité.
4) Qu’est-ce que la densité de mots-clés en SEO ?
La densité de mots-clés en SEO mesure la fréquence d'apparition d'un mot-clé dans le contenu d'une page web, tout en maintenant un équilibre pour éviter la sur-optimisation.
5) Qu’est-ce qu’une balise « alt » ?
La balise "alt" est utilisée pour fournir une description alternative à une image dans le code HTML, ce qui permet aux moteurs de recherche de comprendre le contenu de l'image et d'améliorer l'accessibilité du site.
6) Qu’est-ce que la balise « meta description » ?
La balise "meta description" est une balise HTML utilisée pour fournir une description concise du contenu d'une page web, qui s'affiche généralement dans les résultats de recherche pour donner un aperçu du contenu de la page aux utilisateurs.
7) Qu’est-ce que le « nofollow » en SEO ?
Le "nofollow" est un attribut utilisé dans le code HTML pour indiquer aux moteurs de recherche de ne pas suivre le lien vers la page cible, ce qui limite l'impact du lien sur le classement dans les résultats de recherche.
8) Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
Le contenu de qualité est essentiel pour le référencement d'un site web car il attire les utilisateurs, favorise l'engagement, et améliore la visibilité et le classement dans les résultats de recherche.
9) Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
Il est important d'utiliser des balises de titre de manière structurée car elles aident les moteurs de recherche à comprendre la structure et le contenu de la page, ce qui favorise un meilleur classement. De plus, elles permettent aux utilisateurs de naviguer facilement dans le contenu et d'obtenir une vision claire de l'organisation de l'information.
10) Quelle est la recommandation pour les URL d'un site web bien référencé ?
Pour un site web bien référencé, il est recommandé d'utiliser des URLs conviviales (avec slugs), descriptives et lisibles par les utilisateurs et les moteurs de recherche. Il est également conseillé d'inclure des mots-clés pertinents dans les URLs pour améliorer la compréhension du contenu par les moteurs de recherche.
11) Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
Le maillage interne consiste à créer des liens internes entre les différentes pages d'un site web, ce qui facilite la navigation pour les utilisateurs et permet aux moteurs de recherche de découvrir et d'indexer plus facilement le contenu du site.
Page 20 sur 22
12) Qu'est-ce que l'optimisation des images pour le référencement ?
L'optimisation des images pour le référencement consiste à réduire la taille des fichiers image, à utiliser des balises alt descriptives et à choisir des noms de fichiers pertinents, afin d'améliorer la vitesse de chargement des pages et de permettre aux moteurs de recherche de comprendre et d'indexer correctement le contenu des images.
13) Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?
Un plan de site (sitemap) est un fichier XML ou une page web qui répertorie toutes les pages d'un site web de manière structurée améliorant ainsi leur visibilité dans les résultats de recherche. Un plan de site bien conçu peut également fournir des informations supplémentaires aux moteurs de recherche, telles que la fréquence de mise à jour des pages, les priorités relatives et les métadonnées associées.

## Gestion de projets / DevOps

1) Qu’est-ce que la gestion de projet ?
La gestion de projet est une discipline qui consiste à planifier, coordonner et contrôler les différentes étapes d'un projet afin d'atteindre les objectifs fixés dans les délais impartis. Elle implique l'allocation des ressources, la gestion des risques et la communication entre les parties prenantes pour assurer la réussite du projet.
2) Qu’est-ce qu’une méthode Agile de gestion de projet ?
Une méthode Agile de gestion de projet est une approche itérative et collaborative qui favorise la flexibilité, la réactivité et l'adaptation aux changements. Elle met l'accent sur la livraison continue de produits fonctionnels, la collaboration étroite avec les clients et la révision régulière des objectifs pour répondre aux besoins changeants du projet.
3) Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
La méthode MoSCoW est une technique de priorisation des exigences dans la gestion de projet. Elle divise les exigences en quatre catégories : Must have (doit avoir), Should have (devrait avoir), Could have (pourrait avoir) et Won't have (ne doit pas avoir pour le moment). Les avantages de cette méthode sont sa simplicité, sa clarté dans la définition des priorités et sa capacité à orienter les efforts sur les fonctionnalités essentielles du projet.
4) A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
La méthodologie MVP (Minimum Viable Product) permet de développer et de lancer rapidement un produit avec un ensemble minimal de fonctionnalités nécessaires pour tester son marché et recueillir des retours d'utilisateurs. Les avantages de cette approche sont la réduction des coûts de développement, la validation précoce de l'idée du produit et la possibilité d'itérer et d'améliorer le produit en fonction des retours utilisateurs.
5) Qu’est-ce que la planification itérative ?
La planification itérative est une approche de gestion de projet qui consiste à découper le travail en itérations ou cycles courts, permettant ainsi d'ajuster, d'évaluer et de planifier de manière itérative en fonction des résultats obtenus à chaque étape.
6) Citer 3 méthodes Agiles dans le cadre d’un projet informatique
Trois méthodes agiles couramment utilisées dans le cadre de projets informatiques sont Scrum, Kanban et Extreme Programming (XP).
Page 21 sur 22
7) Qu’est-ce qu’une réunion de revue de projet ?
Une réunion de revue de projet est une rencontre périodique où l'équipe de projet examine l'avancement du projet, évalue les résultats obtenus, identifie les problèmes éventuels et prend des décisions pour la suite du projet.
8) Qu’est-ce qu’un livrable dans un projet ?
Un livrable dans un projet est un élément concret ou une documentation produite à une étape spécifique du projet, qui est livré aux parties prenantes ou aux clients pour validation, utilisation ou évaluation. Cela peut inclure des rapports, des documents, des logiciels, des prototypes, des maquettes, etc.
9) Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
Les trois piliers de Scrum sont la transparence, l'inspection et l'adaptation :
• la transparence permet à tous les membres de l'équipe de collaborer efficacement
• l'inspection permet de contrôler régulièrement l'avancement du projet
• l'adaptation permet d'ajuster le plan et les processus en fonction des retours et des changements.
10) Qu’est-ce que le DevOps et quel est son objectif principal ?
Le DevOps est une approche de développement logiciel qui vise à favoriser la collaboration et l'alignement entre les équipes de développement et d'exploitation, avec pour objectif principal d'accélérer la livraison de logiciels de haute qualité.
11) Qu’est-ce que l’intégration continue ?
L'intégration continue est la pratique consistant à intégrer régulièrement les modifications de code au sein d'un projet afin d'assurer une cohérence et une qualité constantes du logiciel.
12) Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
Docker est une plateforme de conteneurisation qui permet d'emballer une application et ses dépendances dans un conteneur virtuel isolé, ce qui facilite le déploiement et la gestion des applications. Dans le cadre du DevOps, Docker permet une gestion plus efficace des environnements de développement, de test et de production, favorisant ainsi la portabilité, la répétabilité et la scalabilité des déploiements logiciels.
13) Qu’est-ce qu’un test unitaire ?
Un test unitaire est une procédure automatisée visant à vérifier le bon fonctionnement d'une unité de code, généralement une fonction ou une méthode, de manière isolée et indépendante. Il vise à valider le comportement attendu de l'unité de code en testant différentes situations et en comparant les résultats obtenus avec les résultats attendus.
14) Quelle est l'unité de code testée lors d'un test unitaire ?
L'unité de code testée lors d'un test unitaire est généralement une fonction, une méthode ou une classe spécifique. Cependant, cela peut varier en fonction du langage de programmation et de la structure du projet.
15) Quelles sont les caractéristiques d'un bon test unitaire ?
Un bon test unitaire est indépendant des autres tests et de l'environnement, il doit être rapide à exécuter et reproductible. De plus, il doit être spécifique, ciblant une seule fonctionnalité ou un seul comportement à la fois, et fournir des résultats clairs et compréhensibles.
Page 22 sur 22
16) Qu'est-ce qu'une assertion dans un test unitaire ?
Une assertion dans un test unitaire est une expression qui évalue si un résultat obtenu correspond à celui attendu. Elle permet de vérifier la validité d'une condition ou d'une valeur attendue, contribuant ainsi à la vérification de la logique du code testé.

## English

1) What does JavaScript enable you to do on a website ?

- a. Add interactive behavior and dynamic content

2) Which programming language is primarily used for server-side web development ?

- b. PHP

3) What is the purpose of a web browser ?

- a. To render and display web pages

4) What is the difference between GET and POST methods in HTTP ?

- b. GET retrieves data from a server, while POST submits data to a server

5) What is the purpose of version control systems (e.g., Git) in web development ?

- b. To track changes and manage collaborative development

6) What is the purpose of a framework in web development ?

- a. To provide a structured environment for building web applications

7) What does NoSQL stand for ?

- c. Not Only SQL

8) Which of the following is a characteristic of NoSQL databases ?

- b. Strict schema enforcement
