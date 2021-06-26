# Modèle HEIG-VD pour Rapport de Bachelor

Ce référentiel contient le modèle de document pour la production d'un rapport de Bachelor HEIG-VD.

## Utilisation

L'environnement d'édition conseillé est l'éditeur [Microsoft Visual Studio Code](https://code.visualstudio.com/) couplé à [Docker](https://www.docker.com/). Alternativement, il est possible de travailler dans [WSL](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

La distribution LaTeX conseillée est [TeX Live](https://www.tug.org/texlive/). L'alternative MiKTeX est déconseillée.

## Compilation

Ce modèle de document est prévu pour fonctionner avec `xelatex` pour la production d'un fichier `.pdf`. L'outil `latexmk` est utilisé pour séquencer la production du document final. Un `Makefile` s'occupe du prétraitement des figures.

## Prétraitement des figures

Les figures au format `.pdf.svg` sont converties en `.pdf` en utilisant `inkscape`.

Les figures au format `.drawio.xml` sont converties en `.pdf` en utilisant la version desktop de `draw.io`.

Les figures au format `.pdf.py` sont générées à l'aide de Python.

Pour chacun de ces formats un exemple est donné. L'utilisateur final est libre de modifier la logique de production de ces fichiers et d'en ajouter selon ses besoins.

Les conventions de nommage des fichiers intermédiaires sont les suivantes :

| Type | Source | Destination |
|------|--------|-------------|
| Figure vectorielle svg | `.svg` | `.svg.pdf` |
| Diagramme draw.io | `.drawio.xml` | `.xml.pdf` |
| Figure Python | `.py` | `.py.pdf` |

## Bibliographie

## Conventions typographiques et de style

L'ordre conseillé pour le sommaire d'un rapport de Bachelor est le suivant:

1. Préambule
2. Authentification
3. Résumé (français)
4. Résumé (anglais) *optionnel*
5. Table des matières
6. Liste des figures
7. Liste des tables
8. Liste des abbréviations *optionnel*
9. Liste des symboles *optionnel*
10. Introduction
11. Conclusion
12. Glossaire *optionnel*
13. Bibliographie
14. Annexes *optionnel*
15. Index
16. Colophon *optionnel*

Les termes utilisés sont les suivants :

| Terminologie anglaise | Terminologie française | Alternative française |
|-----------------------|------------------------|-----------------------|
| Abstract | Version abbrégée | Résumé |
| Preamble | Préambule | |
| Authentication | Authentification | |
| Content | Table des matières | Sommaire |
| Appendices | Appendices | Annexes |
| Appendix | Annexe | |

Les conventions consensuelles d'usage sont les suivantes :

### Numérotation des pages

- La première et dernière page de couverture ne sont pas numérotées
- Les pages vide ne sont pas numérotées
- Les pages précédant le premier chapitre du document sont numérotées en chiffres romains.
- Les pages à partir du premier chapitre du document sont numérotées en chiffres indo-arabes.

### Numérotation des éléments

- Les tables et les figures sont numérotées selon la convention `chapitre.id` où chapitre est le numéro courant du chapitre et `id` un compteur redémarré à `1` à chaque nouveau chapitre.

### Outils utiles

- Éditeur d'équation en ligne [latex3technics](https://www.latex4technics.com/)
- Éditeur de diagrammes en ligne [draw.io](https://app.diagrams.net/)
- Éditeur de tables pour LaTeX [tablegenerator](https://www.tablesgenerator.com/)
- Éditeur LaTeX en ligne [overleaf](https://www.overleaf.com/)
- Correcteur orthographique compatible LaTeX : [Druide Antidote](https://www.antidote.info/en/antidote-10)

### Conventions typographiques

- Les ligatures sont souhaitées.
- Les paragraphes sont soit indentés, soit espacés, mais pas les deux.
- Le premier paragraphe d'une section n'est jamais indenté.
- En français, les énumérations utilisent le [tiret demi-cadratin](https://fr.wikipedia.org/wiki/Tiret) (`U+2013`).
- Une énumération non ordonnée est considérée comme une phrase continue, chaque entrée sera ponctuée d'une virgule ou d'un point virgule.
- Une énumération ordonnée peut être constituée de phrase complètes.
- Les unités de mesure sont espacée de la grandeur associée par une [espace insécable](https://fr.wikipedia.org/wiki/Espace_ins%C3%A9cable) et ne sont pas en italique ni placées entres crochets.
- Les majuscules sont accentuées comme le recommande l'académie Française.
- Et cetera s'écrit `etc.` et est toujours précédé d'une virgule dans une énumération. La locultion peut être remplacée par des points de suspension `...`. En aucun cas, ces deux formes sont combinées (`etc...`). Les points de suspension sont toujours collés dernier caractère d'une liste énumérée. (`a, b, c...`).
- Les mots étrangés ou les anglicismes sont placés en italique.

### Locutions

- La locution *confer* (voir ceci) est abrégée `cf.`
- La locution *id est* (c'est à dire) est abrégée `c.-à-d.` et non `i.e.`
- La locution *exempli gratia* (pour l'exemple) est abrégée `p. ex.` et non `e.g.`

Les locutions latines non francisées suivantes seront écrites en italique :
*ad hoc*, *ad libitum*, *a fortiori*, *a posteriori*, *a posteriori*, *a priori*, *bis*, *grosso modo*, *ibidem*, *idem*, *in extenso*, *in extremis*, *in extenso*, *in extremis*, *in fine*, *infra*, *loc.cit.*, *modus vivendi*, *op.cit.*, *passim*, *quater*, *sic*, *statu quo*, *supra*, *ter*, *via*, *vice versa*.
### Standards

- Diagrammes BPMN 2.0 (*Business Process Model And Notation*) [specification](https://www.bpmn.org/)
- Diagrammes UML 2.5.1 (*Unified Modelling Language*) [specification](https://www.omg.org/spec/UML/About-UML/)

### Références

- [Petites leçons de typographie](https://jacques-andre.fr/faqtypo/lessons.pdf) de Jaques André
- [Lexique des règles typographiques en usage à l’Imprimerie
nationale](https://www.payot.ch/Detail/lexique_des_regles_typographiques_en_usage_a_limprimerie_nationale-collectif-9782743304829) de l'Imprimerie Nationale française. ISBN 2-7433-0482-0