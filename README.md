# dahprojects
**Digital art history projects directory | Répertoire de projets en histoire de l’art numérique**

Auteurs :

- Emmanuel Château-Dutier (Orcid : [0000-0003-4092-4569](https://orcid.org/0000-0003-4092-4569)),
- Léa Maronet (Orcid : [0009-0005-2532-5375](https://orcid.org/0009-0005-2532-5375))

Financeurs :

- [Ouvroir d’histoire de l’art et de muséologie numériques](https://ouvroir.umontreal.ca), [Centre de recherche interuniversitaire sur les humanités numériques](https://www.crihn.org)

## Constitution du corpus

Ce répertoire vise à documenter de manière exhaustive les projets menés en histoire de l’art numérique à l’échelle internationale depuis l’avènement du world wide web. Il s’intéresse aux recherches qui mobilisent des méthodologies numériques en histoire de l’art à partir d’un repérage sur le web et en compilant diverses sources bibliographiques. Il faut d’emblée souligner que son périmètre actuel se limite aux projets qui disposent d’une vitrine sur le web. Les projets de diffusion de collections muséales numérisées ou de médiation numérique n’ont pas été inclus.

L’étabilissement de ce répertoire utilise la [Text Encoding Initiative (TEI)](https://tei-c.org/) pour la description des entrées. Les projets sont en cours de catégorisation avec la taxonomie des activités de recherche numériques dans les humanités [TADIRAH](https://tadirah.info/) et les entrées thématiques du [Répertoire unifié de vedettes matières de la bibliothèque nationale de France](https://rameau.bnf.fr/informations/rameauenbref) à partir de [DataBnf](https://data.bnf.fr/fr/vocabulary/rameau/).

## Structuration du répertoire

```
sites
├── dahprojects.tei.xml # directory
├── documentation # documentation
└── schema # schemas XML
```

## Interface de publication

(en cours de production)

L’interface de publication permet de consulter la liste des projets et leurs notices en proposant différents points d’accès (chronologiques ou thématiques). La création du répertoire permet également d’envisager les développements de l’histoire de l’art numérique de manière critique et réflexive en utilisant des outils de visualisation. L’exploitation quantitative des projets réclame donc une attention particulière à l’établissement des catégories pour privilégier au maximul l’utilisation de catégories disjointes.

Fiche de projet

Liste des projets

Filtres avec quantificateurs

- chronologiques
- thématiques
  - géographiques
  - disciplinaires
  - périodisation
- filtre dynamique (recherche simple)

Tri des listes de projets

- par date de création
- par ordre alphabétique de titre

Champ de recherche simple

Dataviz

- chronologie
- géographique

### Choix technologiques

Plusieurs options possibles : 

- une chaîne de transformation basée sur XSLT avec l’utilisation de JavaScript pour les filtres, etc.
- une chaîne de transformation basée sur XSLT avec l’utilisation de SaxonJS pour les interactions utilisateurs (côté client)
- une chaîne de transformation basée sur XSLT avec l’utilisation de HTMX pour les interactions utilisateurs (ce qui implique peut-être de disposer d’un serveur)
- transformation des contenus en JSON et création d’un client Svelte (approche statique)

XML --> XSL --> HTML

- Une page par notice
- Une page par liste (mais complication pour produire les filtres avec JavaScript, car travail directement sur les éléments Html, à moins d’utiliser Saxon)
- travailler les filtres en JavaScript

XML --> XSL --> JSON + Svelte

