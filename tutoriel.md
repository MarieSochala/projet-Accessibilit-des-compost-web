# L'accessibilité des composants Web

## 1. Qu'est ce que l'accessibilité ?

L'accessibilité, c'est celle de son site Internet bien sûr, mais qu'est-ce que c'est que ce truc ? A quoi ça sert ? Et puis pourquoi faut-il qu'un site soit accessible ?  

Le but est de créer des applications et du contenu web riche (qui inclut ajax et javascript et mis à jour dynamiquement) en le rendant accessible aux personnes handicapées car l'accessibilité est un droit universel. 

Ainsi :
        
* Lorsqu'un site respecte les règles d'accessibilité, Michel, handicapé moteur, peut naviguer sur les pages sans jamais utiliser de souris, avec le clavier traditionnel ou un dispositif adapté..   
* Lorsqu'un site respecte les règles d'accessibilité, Julien, aveugle, peut écouter le contenu de chaque page lue par son navigateur vocal, et naviguer à l'aide des indications données par celui-ci.    
* Lorsqu'un site respecte les règles d'accessibilité, Papi et Mamie ne sont pas gênés par la taille des textes, ils peuvent utiliser la fonction de “grossissement des textes” de leur navigateur.
         
Enfin, le respect des critères techniques d'accessibilité ne bénéficie pas qu'aux publics handicapés. En effet, ces critères recoupent pour une large part ceux, plus généraux, de la qualité des services en ligne : chacun y trouvera son compte, avec une meilleure navigabilité, une ergonomie plus ouverte, un Web plus intuitif et d'un abord moins complexe.      https://github.com/MarieSochala/projet-Accessibilit-des-compost-web.git

## 2.Comment rendre son site accessible ?

Afin de répondre à ce besoin, la norme ARIA a été créée, et fonctionne avec HTML 5. ARIA est l’abréviation de l’anglais Accessible Rich Internet Applications suite. C'est une norme qui via l'ajout de nouveaux attributs permet de rendre les contenus plus accessibles aux personnes en situation de handicap. 
         
Les différents composants d'un site se doivent d'être accessible, tels que :         
    
* Fenêtres modales (popins)    
* Boîtes de dialogue modales (popins de dialogue)    
* Boîtes d’alerte modales (popins d’alerte)    
* Boutons « Afficher plus »    
* Boutons radio simulés en ARIA    
* Boutons radio simulés en CSS    
* Carrousels    
* Cases à cocher simulées en ARIA   
* Accordéons    
* Cases à cocher simulées en CSS    
* Infobulles simulées en ARIA    
* Onglets    
* Panneaux dépliants    
* Sliders simulés en ARIA    
* Spinbuttons (boutons fléchés) simulés en ARIA
              
Voici une check-list exhaustive de tout ce qu'il y a à respecter pour qu'un site soit parfaitement accessible :  http://checklists.opquast.com/oqs-v3/COMMENT :      
    
* Ecrire le contenu de manière claire et concise et l'organiser de façon logique et facile à comprendre.      
* Utiliser des polices, tailles de texte de manière uniforme dans le site, et les choisir en sorte qu'elles soient facilement lisibles.    
* Couleurs adaptées aux différents problèmes de vision. Faire attention à ce qu'il y ai un contraste suffisant. Ne pas utiliser des couleurs seules pour dispenser une information.    
* Eviter les visuels répétitifs ou flashant, et mettre en place une possibilité de désactiver les éléments flashant ou bougeant.    Marquer les éléments de manière à ce que les applications d'accessibilité puissent les lire.     Faire en sorte qu'il soit possible de naviguer uniquement à l'aide du clavier.    
* Faire des sites responsives, adaptés aux différents écrans et supports de navigation, ordinateurs anciens, connexions lentes.     Utiliser des tailles relatives (en pourcentages par exemple) pour les éléments, afin que si l'utilisateur modife la taille du texte la page s'adapte.    
* Prendre en compte les éléments HTML utilisés pour lire le contenu                      
* META tags pour décrire et identfier le contenu   :  ( LISTE DES META TAGS : http://www.objectif-referencement.com/comprendre.php )
* ALT  tags  pour décrire des images, acronymes, longs textes etc   
* Tags pour les langues, <span lang="en"> pour une citation et <html lang=fr"> pour la page    Utiliser les tags à notre disposition comme <ACRONYM title=""> et <ABBR title=""> pour les acronymes et les abbréviations, mettre des <label> aux inputs des formulaires    
* Boutons et éléments cliquables assez grands pour qu'ils puissent être cliqués sans devoir cibler de manière précise 
* Elements commes les liens et boutons créés de manière à ce que leur nature soit évidente   
* Mettre un texte alternatif pour le contenu sonore ou visuel, vérifier que sans son le contenu fonctionne toujours    
* Eviter les éléments avec un délai d'intéractions 


### a. Document landmarks ou Sections du document
Pour structurer un document, ARIA définit les rôles des zones du document:

-article
    Contenu ayant du sens par lui-même, comme un article ou un commentaire de blog, 	un message sur un forum, etc.
-banner
    Contenu à propos du site, comme le titre de la page ou le logo.
-complementary
    Permet éventuellement de définir une partie du contenu principal, mais est plus 	approprié pour du contenu séparé : la météo sur un portail web par exemple.
-contentinfo
    Contenu dépendant d’un autre, comme des notes de bas de page, un copyright, un 	lien vers la déclaration de confidentialité, un lien vers les paramètres de 	l’application, etc.
-main
    Contenu directement lié ou englobant le contenu central du document.
-navigation
    Contient des liens pour naviguer dans ou en dehors du document.
-search
    Cette section contient un formulaire de recherche permettant de chercher sur le 	site. 

```Html
<div role="banner">
...
</div>
<div role="navigation">
...
</div>
<div role="main">
...
</div>
```



    
## 3. Exemple concret

Voici un exemple de code non accessible :     
```
<div >    
    <h1>Titre de ma page</h1>    
    <h2>Sous-titre de ma page</h2>
</div>
<div>
    <div>    
        <h3>Titre de l’article</h3>    
        <p>Un premier paragraphe</p>   
        <p>Un second paragraphe</p>
    </div>
    <div>
        <h3>Titre de l’article</h3>    
        <p>Un premier paragraphe</p>    
        <p>Un second paragraphe</p>https://github.com/MarieSochala/projet-Accessibilit-des-compost-web.git
    </div>
</div>
<div >    
    <h3>Édito du jour</h3>    
    <p>Un premier paragraphe</p>    
    <p>Un second paragraphe</p>    
    <h3>Liens utiles</h3>
    <ul>    
        <li><a href="/1">Lien 1</a></li>    
        <li><a href="/2">Lien 2</a></li>    
        <li><a href="/3">Lien 3</a></li>
    </ul>
</div>   
<div id="footer">    
    <p>Site réalisé par Môaa...</p>
</div>
```
Voici un code accessible :    
```
<header role="banner">    
    <hgroup>    
        <h1>Titre de ma page</h1>    
        <h2>Sous-titre de ma page</h2>    
    </hgroup>
</header>
<div id="content" role="main">    
    <article>    
        <h3>Titre de l’article</h3>    
        <p>Un premier paragraphe</p>    
        <p>Un second paragraphe</p>    
    </article>    
    <article>    
        <h3>Titre de l’article</h3>    
        <p>Un premier paragraphe</p>   
        <p>Un second paragraphe</p>    
    </article>
</div>

    <!--fin content-->

<aside role="complementary">    
    <section>    
        <h3>Édito du jour</h3>    
        <p>Un premier paragraphe</p>    
        <p>Un second paragraphe</p>    
    </section>    
    <section>    
        <h3>Liens utiles</h3>    
        <ul>    
            <li><a href="/1">Lien 1</a></li>    
            <li><a href="/2">Lien 2</a></li>    
            <li><a href="/3">Lien 3</a></li>    
        </ul>
    </section>
</aside>
<footer role="contentinfo">    
    <p>Site réalisé par Môaa...</p>
</footer>
```

## 4. L'attribut tabindex

L'attribut tabindex permet de naviguer de lien en lien, a l'aide de la touche tabulation.

**Exemple :**

```
<a href="monlien" tabindex="1"></a>
<a href="autrelien" tabindex="2"></a>
```

Dans l'exemple ci-dessus, en appuyant sur la touche tab une fois on sera sur "monlien", et en appuyant une deuxième fois on arrivera sur "autrelien". 
## 5. Sources et liens utiles 

On peut également rendre accessible un élément sans utiliser la norme ARIANos sources : 

http://www.acsu.buffalo.edu/~dbertuca/ada/web-access.html

http://code.tutsplus.com/tutorials/accessibility-part-3-aria--cms-21793

http://www.lesintegristes.net/2008/12/09/introduction-a-wai-aria-traduction/

http://www.accede-web.com/Wikipedia

Sites de test accessibilité de pages web

http://www.open-s.com/fr/content/tanaguru-axs

http://wave.webaim.org//

http://reporting.opquast.com/en/inspector/
