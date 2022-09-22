# Accessibility

## Présentation


## Un lecteur d'écran
Un lecteur d'écran (screenReader) est un logiciel qui lit le contenu d'une page web et le restitue au moyen d'une synthèse vocale ou de braille. Le contenu qui est transmis ne se limite pas au texte qui est affiché. Le lecteur d'écran transmet également de l'information sémantique. Il lira par exemple 'Actualités titre de niveau 2' ou 'lien visité Contact'. Tout ce contenu est mis à la disposition du lecteur d'écran par les navigateurs par l'intermédiaire de l'accessibility tree.

L'accessibility tree est une structure, construite sur base du code source et des scripts, comme le DOM, mais qui

- ne contient pas les information inutiles pour l'accessibilité (le lecteur d'écran n'a pas besoin de savoir qu'il y a 15 div imbriqués)
- associe à chaque élément un rôle, un nom et un état.

Pour les éléments HTML standards (img, button, h1,...) ces informations sont disponibles par défaut. Par exemple pour le <button>Search</button>, les informations remplies dans l'accessibility tree sont:

- Rôle: button,
- Nom: Search,
- Statut: unselected.
- Propriété : focusable

Sur base de ces informations, l'internaute sait de quelle manière il peut interagir avec le contenu.

(Voir exemple 1)

## Améliorer l'accéssibilité avec ARIA
Pour les composants d'interfaces riches, qui sont composés d'éléments HTML standards, les informations qui se trouvent dans l'accessibility tree sont insuffisantes. Elles ne permettent pas de comprendre la nature du composant complexe et d'anticiper son comportement. Un module d'onglets sera vu par le lecteur d'écran comme une liste de liens suivie d'un paragraphe de texte. Rien ne permettra à l'utilisateur du lecteur d'écran d'anticiper que le contenu de ce paragraphe est modifié chaque fois qu'un des liens est activé. Rien n'indique que ces éléments forment un tout, ni quelle est la nature de ces composants.

ARIA complète HTML afin que les éléments interactifs et les widgets puissent être utilisés par les outils d'assistance quand les fonctionnalités standard ne le permettent pas. Ainsi, ARIA permet de rendre accessible les widgets JavaScript, les indications dans les formulaires, les messages d'erreur et les mises à jour dynamiques du contenu, etc.

Les attributs ARIA peuvent servir à compléter l'information de l'accessibility tree, pour rendre les interfaces riches compréhensibles et utilisables avec un lecteur d'écran. Les attributs ARIA peuvent aussi écraser des informations dans l'accessibility tree, et c'est pour celà qu'il faut les utriliser avec la plus grande prudence.

(Voir exemple 2)

## Exemples de ce que les attributs ARIA peuvent faire
- améliorer l'accessibilité de composants (comme les onglets) pour lesquels il n'existe pas de balises HTML spécifiques.
- communiquer un statut qui est visuellement très clair mais qui n'est pas annoncé par un lecteur d'écran, par exemple si un sous-menu est déplié ou pas.
- faire annoncer à un lecteur d'écran qu'une information est apparue ou a été mise à jour ailleurs sur la même page.
- nommer plus clairement des éléments d'une page (ou application) web pour les personnes aveugles qui n'ont pas la vue d'ensemble de la page.
- ajouter de l'information sémantique qui n'existe pas (encore) en HTML. 

(Voir exemple 3)

## Présentation de comportement de site adapté pour les handicaps visuelles. 
- http://google.be/search
- https://fr.wikipedia.org/wiki/Recette#content
- https://developer.mozilla.org/fr/

(En pressant tab d'entrée sur ces sites vous faites apparaitres un petit menu en haut à gauche qui vous permet d'atteindre le contenu principal de la recherche)