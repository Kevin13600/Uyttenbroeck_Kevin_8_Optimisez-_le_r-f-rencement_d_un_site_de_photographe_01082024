Etape 1 : Prenez en main le code source

code récupéré.
Prise en compte de l'enoncé.
Première analyse du code avec Lighthouse.

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