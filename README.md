# 🚀 Créer et administrer un site sous le cms WordPress

## <strike>Introduction</strike>

-> L'introduction arrivera plus tard, passons tout de suite à la pratique 🎮


## Télécharger WordPress
Disponible gratuitement, vous pouvez le télécharger à l'adresse : https://fr.wordpress.org/download/

WordPress nécessite un serveur web capable d'exécuter le PHP et un serveur de base de données de type SQL pour fonctionner

Téléchargez l'archive et décompressez la dans votre espace de travail, c'est à dire là où vous rangez vos projets web 😉

Le dossier de l'archive s'appelle wordpress, vous pouvez le renommer en **td-wordpress-s3**

Ouvrez maintenant le projet depuis votre serveur web, vous arriverez sur l'étape d'installation de Wordpress :

<img width="801" alt="setup-1" src="https://user-images.githubusercontent.com/3802323/140843198-0152b790-d696-44bb-8400-e74131a7ff91.png">

Cliquez sur `C'est parti !`pour accéder à l'étape suivante : 

<img width="809" alt="setup-2" src="https://user-images.githubusercontent.com/3802323/140843454-dc2c408f-67ee-4ce6-81c1-1460334342ad.png">

Vous devez maintenant saisir les informations de connexion à votre base de données, la base de données n'existe pas encore, je vous propose donc de la créer à l'aide de phpMyAdmin, vous pouvez l'appeler **td-wordpress-s3**, revenez ensuite à l'étape d'installation pour compléter les informations

<img width="795" alt="setup-3" src="https://user-images.githubusercontent.com/3802323/140844001-6b36c2cf-cea6-4480-800b-6b36ae6bbd46.png">

Passez à l'étape suivante de l'installation, vous allez devoir renseigner le nom de votre site, un identifiant, un mot de passe et une adresse mail pour créer l'administrateur du site, je vous propose d'entrer les informations suivantes : 

**Titre du site :** La frite c'est la fête 🍟

**Identifiant :** etudiant

**Mot de passe :** mmi

**Adresse de messagerie :** etudiant@mmi.cool

Vous devrez confirmer l'utilisation d'un mot de passe faible, inutile de vous rappeler que nous n'utilisons pas ce genre de mot de passe en production 😱

<img width="798" alt="setup-5" src="https://user-images.githubusercontent.com/3802323/140845075-ed5a649c-6602-45ff-a55a-6059cc5b6e69.png">

Et voilà ! WordPress est installé ! Vous pouvez vérifier en consultant le site tout simplement 🥳


## Dépôt git
Nous allons initialiser un nouveau dépôt git sur la plateforme GitHub pour accueillir votre projet, je vous invite à vous rendre à l'adresse https://github.com et vous y connecter.

Cliquer sur `new repository` ou aller directement à l'adresse suivante pour créer un nouveau dépôt : https://github.com/new

Choisissez un nom de dépôt en complétant le champs `Repository name`, par exemple : **td-wordpress-s3**

Je vous laisse le choix du dépôt publique ou privé !

Rendez-vous ensuite dans les paramètres du dépôt en cliquant sur `Settings` puis dans l'onglet `Manager access`, cliquez sur `Add people` pour m'ajouter en tant que collaborateur sur votre projet, voici mon nom d'utilisateur : **sulli-a**

Ouvrez votre terminal préféré et aller dans le dossier de votre projet puis executer les commandes suivantes :

On initialise le dépôt : 
```
git init
```

On ajoute tous les fichiers de notre projet (nous pourrons plus tard en exclure à l'aide du fichier .gitignore) :
```
git add -A
```

On effectuer notre premier commit avec le message de notre choix : 
```
git commit -m "Initialisation du projet !"
```

Vous pouvez ensuite recopier les commandes proposés directement par GitHub : 

⚠︎ **Ne pas recopier** les commandes ci-dessous ⚠︎

```
git branch -M main
git remote add origin git@github.com:votreNomUtilisateur/votreRepo.git
git push -u origin main
```

## Administration et introduction 
Rendez-vous à l'adresse de votre site pour le consulter, vous accéderez à l'interface d'administration en ajoutant **/wp-admin** dans l'adresse, exemple : *http://localhost/td-wordpress-s3/wp-admin*

Pour vous connecter, vous pouvez utiliser le compte administrateur crée lors de l'installation 

Un CMS (Content Management System) est un système de gestion de contenu, il nous permet de mettre en page, d’éditer toutes sortes de contenu et nous propose un lot de fonctionnalités prêtes à utiliser : interfaces d’administration de contenu, authentification des utilisateurs et gestion des rôles, gestion des médias, articles d’un blog, commentaire, formulaires...

Plus concrètement, utiliser un CMS vous permet de gagner du temps lorsque vous souhaitez créer un site web avec une interface d’administration des contenus, vous pourrez vous focaliser sur la partie front-end plutôt que développer un back-end sur mesure.

Note : l’interface d’administration sera utilisée par votre client, elle se doit d’être simple à utiliser, il est hors de question que le client fasse du code 😉

Sur le marché, il existe plusieurs CMS, pour en citer quelques uns : Drupal, Typo3, Hugo, eZ Platform...

D’après les statistiques de W3Techs, WordPress est le CMS le plus utilisé au monde avec 65.1%% d’utilisation des CMS sur le marché et 42.8% de tous les sites confondus. Il y a donc de fortes chances que vous rencontrerez WordPress dans le monde professionnel; que vous vous orientez dans un cursus de communication, d’ingénierie web ou peut-être pour proposer et/ou vendre vos propres services et/ou produits 😀

Revenons à l'interface d'administration, nous retrouvons 3 principaux types de contenu :

- Article (post*) : les articles correspondent aux actualités et/ou la partie blog de votre site.
- Média (attachment*) : les médias de votre site, images, musiques, vidéos...
- Page (page*) : les pages contiennent du contenu en tout genre : textes, images, formulaires...

* Techniquement ceux sont les noms des types de contenu (post type), nous verrons plus tard qu’il est possible de créer des nouveaux types de contenu (Custom Post Type).


## Exercice
Vous allez réaliser votre site portfolio, rien que ça et vous verrez cela vous prendra très peu de temps !

Télécharger l'archive **s3-site.zip** qui se trouve dans ce dépôt git, il s'agit d'un exemple de site portfolio que vous pouvez réaliser, libre à vous de changer les styles et le contenu bien sur 😉

Pour commencer à éditer votre portfolio, depuis l'interface d'administration rendez-vous dans `apparence -> personnaliser`

Depuis l'outil personnaliser, vous allez pouvoir changer le titre et slogan du site, par exemple : Portfolio de XX, modifier certains styles de votre site...

Pour éditer ensuite le contenu des pages, il faudra vous rendre dans la rubrique `page`, et sélectionner la page que vous souhaitez éditer

Pour éditer les images de votre site, vous pouvez accéder à la médiathèque en cliquant sur lien `médias`dans la barre latérale

Pour éditer le contenu de votre blog, vous cliquerez sur le lien `articles` 

<br><br><br><br><br><br>


# Part 2

## Créer votre thème !

Commencez par télécharger l'archive `fondation.zip` pour découvrir la template à partir de laquelle vous allez réaliser votre thème

Ouvrez-ensuite votre projet à partir de votre éditeur de code favori

Les thèmes WordPress sont situés dans le dossier `wp-content/themes/`

Un thème nécessite seulement 2 fichiers pour fonctionner, bon ce ne sera pas un thème très complet mais une bonne base pour découvrir son fonctionnement 😉

Créer le dossier de votre thème, `theme-mmi` par exemple, appelez-le comme vous voulez :-)

Dans le dossier de votre thème, créer les 2 fichiers suivants : 

styles.css :
```
/*
Theme Name: theme-mmi (nom de votre thème)
Author: Vous ! (votre petit nom)
Description: Description (description de votre thème)
Version: 1.0.0
Text Domain: theme-mmi (nécessaire si nous créons un thème multi-langue)
*/
```
index.php :
```
<h1>Hello MMI !</h1>
```

Ces deux fichiers sont le minimum requis pour que WordPress détecte le thème et l'affiche dans la liste des thèmes. 

Vous pouvez maintenant vous rendre dans le backend puis dans le menu latéral cliquer sur `Apparence -> Thèmes` pour activer votre thème.

`Bonus : Pour attacher un visuel à votre thème, vous pouvez ajouter une image dans le dossier de votre thème et la renommer screenshot.png`

## La base et la loop
Consultez le front-office de votre site, vous devriez retrouver le contenu d'**index.php**.

Nous allons créer le header et le footer de notre thème afin de les inclure dans notre page blanche.

Créez les fichiers `header.php` et `footer.php`

Le fichier `header.php` contiendra le haut de notre page et le fichier `footer.php` le bas. Dans `index.php`, il nous suffira alors de les inclure.

header.php : 
```
<!doctype html>
<html <?php language_attributes(); ?>>
<head>
	<meta charset="<?php bloginfo( 'charset' ); ?>">
	<meta name="viewport" content="width=device-width, initial-scale=1">

	<?php wp_head(); ?>
</head>

<body <?php body_class(); ?>>
```

footer.php :
```
<footer>
  <p>&copy; Tous droits réservés</p>
</footer>
<?php wp_footer(); ?>

</body>
</html>
```

`Vous remarquerez une particularité, la balise body est ouverte dans le header et est
fermée dans le footer.`

Pour inclure le header et le footer dans notre template, nous ferons appel aux
méthodes `get_header()` et `get_footer()` dans `index.php`

index.php
```
<?php get_header(); ?>

<h1>Hello MMI !</h1>

<?php get_footer(); ?>
```

Enfin pour afficher le contenu de notre page plutôt que Hello MMI !, nous utiliserons The_Loop (la boucle) de WordPress, voir la documentation : https://developer.wordpress.org/themes/basics/ the-loop/


```
<?php
  if ( have_posts() ) : // Si il y a du contenu à afficher

    /* Start the Loop */
    while ( have_posts() ) : // Boucle sur l'ensemble des contenus, si on consulte la page blog par exemple, nous allons itérer sur toutes les actualités
      the_post();

      the_title(); // Affiche le titre du contenu en cours dans la loop

    endwhile;

  endif;
?>
```

## Paramétrage du thème

Pour configurer notre thème, nous allons créer le fichier `functions.php` qui embarquera l’ensemble des fonctions php et paramètres de notre thème, déclaration de menus, nouveau type de contenu, chargement de fichiers...

Commençons par créer le dossier `assets` dans lequel nous allons créer 3 dossiers pour stocker nos images (`img`), nos feuilles de styles (`css`) et nos fichiers javascript (`js`)

Cela donne l'arborescence suivante : 

```
assets
- img
- css
- js
```

Créer le fichier `functions.php`
```
<?php
/**
 * Enqueue scripts and styles.
 */
function theme_mmi_scripts() {
  // Exemple pour charger une feuille de styles, get_template_directory_uri() nous renvoie le chemin du thème, nous concaténons ensuite le chemin jusqu'au fichier qui nous intéresse
	wp_enqueue_style( 'theme-mmi-style', get_template_directory_uri() './assets/css/styles.css', array(), 1.0 );
  
  // Exemple pour charger un fichier javascript
  wp_enqueue_script( 'theme-mmi-script', get_template_directory_uri() . '/assets/js/example.js', array(), 1.0, true );
}
add_action( 'wp_enqueue_scripts', 'theme_mmi_scripts' );
```

`Ci-dessus, la méthode `wp_enqueue_style()` nous permet de charger des ressources css et la méthode `wp_enqueue_script()`des ressources js, notez que dans les 2 cas le 1er paramètre passé à la méthode est un identifiant unique`

Si tout se passe bien et que le fichier de styles existe, vous devriez voir les premiers styles de votre thème, bravo ! 👏

## Déclarer un menu

Dans le fichier `functions.php`, vous allez utiliser la méthode `register_nav_menus()` pour déclarer un ou plusieurs nouveau menu

```
register_nav_menus(
  array(
    'identifiant_menu' => 'Intitulé du menu que je retrouve dans le back-office',
  )
);
```

Pour afficher un menu, nous utiliserons la fonction `wp_nav_menu()` https:// developer.wordpress.org/reference/functions/wp_nav_menu/

En appelant cette méthode, il faut lui préciser quel menu nous souhaitons afficher (menu principal dans le header par exemple), on peut lui passer en paramètre l’identifiant du menu que vous avez utilisé lors de sa création à l’aide de la fonction `register_nav_menus()`

## Exercice

Commencez par intégrer la page blog dans votre thème 🚀
