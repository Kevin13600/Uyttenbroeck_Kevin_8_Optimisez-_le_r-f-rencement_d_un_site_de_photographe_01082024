Etape 1 : Prenez en main le code source

code récupéré.
Prise en compte de l'enoncé.
Première analyse du code avec Lighthouse.

---------------------------------------------------------------------------

Etape 2: Listez les optimisations qui peuvent être realisées

Performances:

Fichiers JavaScript (scripts.js, bootstrap.bundle.js, maugallery.js) :

Réduisez les ressources JavaScript inutilisées
Réduisez la taille des ressources JavaScript
Évitez de créer des chaînes de requêtes critiques
Réduire le travail du thread principal
Évitez les tâches longues dans le thread principal

Fichiers CSS (style.css, bootstrap.css) :

Réduisez la taille des ressources CSS
Réduisez les ressources CSS inutilisées

Fichiers images (dans le dossier images) :

Dimensionnez correctement les images
Encodez les images de manière efficace
Diffusez des images aux formats nouvelle génération
Les éléments d'image ne possèdent pas de width ni de height explicites

index.html :

Éliminez les ressources qui bloquent le rendu
Évitez une taille excessive de DOM
Évitez les changements de mise en page importants
Les éléments d'image ne possèdent pas de width ni de height explicites

Configuration du serveur :

Diffusez des éléments statiques grâce à des règles de cache efficaces
Le temps de réponse initial du serveur était court

Général (peut impliquer plusieurs fichiers) :

Évitez d'énormes charges utiles de réseau
Réduire au maximum l'utilisation de code tiers


Accessibilité : 


Des éléments d'image n'ont pas d'attribut [alt]
Le document ne contient pas d'élément <title>
Les éléments de formulaire ne sont pas associés à des libellés
Les liens n'ont pas de nom visible
Les couleurs d'arrière-plan et de premier plan ne sont pas suffisamment contrastées
L'élément <html> n'a pas d'attribut [lang]
Les éléments d'en-tête ne sont pas classés séquentiellement par ordre décroissant

SEO: 


Le document ne contient pas d'élément <title>
Le document ne contient pas d'attribut "meta description"
Des éléments d'image n'ont pas d'attribut [alt]

-------------------------------------------------------------------------------------------

Etape 3: Optimisation performance

Optimisations apportées au fichier index.html :

///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Utilisation de la technique de chargement asynchrone pour les feuilles de style CSS avec rel="preload" et onload, ce qui réduit le blocage du rendu.
Explications :

1. rel="preload" : Indique au navigateur de commencer à charger le fichier CSS immédiatement, mais sans bloquer le rendu de la page.
2. as="style" : Spécifie que la ressource préchargée est une feuille de style.
3. onload="this.onload=null;this.rel='stylesheet'" : Une fois le fichier CSS chargé, cette partie du code change dynamiquement l'attribut rel de "preload" à "stylesheet", appliquant ainsi les styles à la page.
4. La balise <noscript> : Fournit une solution de repli pour les utilisateurs qui ont désactivé JavaScript. Elle assure que les styles seront toujours chargés, même si le chargement asynchrone ne fonctionne pas.
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////



Minification des noms de fichiers CSS et JS (ex: bootstrap.min.css, style.min.css).
Ajout des attributs width et height à toutes les images pour éviter les changements de mise en page importants.
Restructuration du HTML avec des balises sémantiques (<header>, <main>, <section>).
Remplacement de certains <h3> par <h2> pour une meilleure hiérarchie des titres.
Ajout de l'attribut defer aux balises <script> pour différer leur chargement.
Mise à jour de jQuery vers une version plus récente (3.6.0).
Suppression du contenu de la galerie dans le HTML. Les images seront chargées dynamiquement par JavaScript pour réduire la taille du DOM initial.
Ajout des attributs required aux champs du formulaire de contact.
Ajout de l'attribut rel="noopener noreferrer" au lien Instagram pour des raisons de sécurité.

optimisations apportées au fichier CSS :

Regroupement des styles similaires pour réduire la duplication.
Suppression des propriétés redondantes ou inutiles.
Utilisation de sélecteurs plus efficaces.
Simplification des media queries en regroupant les styles communs.
Remplacement de certaines valeurs spécifiques par des valeurs relatives (ex: em au lieu de px) pour une meilleure adaptabilité.
Suppression des commentaires inutiles.
Optimisation de l'ordre des déclarations pour une meilleure lisibilité et maintenance.


Etape 4: Optimisation SEO 


Ajout d'une balise <title> et d'une meta description pour améliorer le SEO.


Etape 6: Optimisation Accessibilité

Ajout de l'attribut lang="fr" à la balise <html> pour spécifier la langue du document.