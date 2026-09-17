---
title: "Aspose::Words::Math::MathObjectType énumération"
linktitle: "MathObjectType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::MathObjectType énumération. Spécifie le type d'un objet Office Math en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Spécifie le type d'un objet Office [Math](../).

```cpp
enum class MathObjectType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| OMath | 0 | Instance de texte mathématique. |
| OMathPara | 1 | [Math](../) paragraphe, ou zone de mathématiques affichée, qui contient un ou plusieurs éléments [OMath](./) en mode affichage. |
| Accent | 2 | Fonction Accent, composée d'une base et d'un signe diacritique combiné. |
| Bar | 3 | Fonction Bar, composée d'un argument de base et d'une barre supérieure ou inférieure. |
| BorderBox | 4 | [Border](../../aspose.words/border/) objet Boîte, composé d'une bordure dessinée autour d'une instance de texte mathématique (comme une formule ou une équation) |
| Box | 5 | Objet Boîte, utilisé pour regrouper les composants d'une équation ou d'une autre instance de texte mathématique. |
| Délimiteur | 6 | Objet délimiteur, composé de délimiteurs ouvrants et fermants (tels que les parenthèses, accolades, crochets et barres verticales), et d'un élément contenu à l'intérieur. |
| Degré | 7 | Degré dans le radical mathématique. |
| Argument | 8 | Objet argument. Enveloppe les entités Office [Math](../) lorsqu'elles sont utilisées comme arguments d'autres entités Office [Math](../). |
| Tableau | 9 | Objet tableau, composé d'une ou plusieurs équations, expressions ou autres séquences de texte mathématique pouvant être justifiées verticalement en tant qu'unité par rapport au texte environnant sur la ligne. |
| Fraction | 10 | Objet fraction, composé d'un numérateur et d'un dénominateur séparés par une barre de fraction. |
| Dénominateur | 11 | Dénominateur d'un objet fraction. |
| Numérateur | 12 | Numérateur de l'objet Fraction. |
| Fonction | 13 | Objet Fonction-Appliquer, qui consiste en un nom de fonction et un élément argument sur lequel il agit. |
| NomFonction | 14 | Nom de la fonction. Par exemple, les noms de fonctions sont sin et cos. |
| CaractèreGroupe | 15 | Objet Groupe-Caractère, composé d'un caractère placé au-dessus ou au-dessous du texte, souvent dans le but de regrouper visuellement les éléments. |
| Limit | 16 | Limite inférieure de l'objet [LowerLimit](./) et limite supérieure de la fonction [UpperLimit](./). |
| LowerLimit | 17 | Objet Limite-Inférieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement en dessous. |
| UpperLimit | 18 | Objet Limite-Supérieure, composé de texte sur la ligne de base et de texte de taille réduite immédiatement au-dessus. |
| Matrice | 19 | Objet matrice, composé d'un ou plusieurs éléments disposés sur une ou plusieurs lignes et une ou plusieurs colonnes. |
| MatrixRow | 20 | Ligne unique de la matrice. |
| NAry | 21 | Objet n-aire, composé d'un objet n-aire, d'une base (ou opérande) et de limites supérieures et inférieures optionnelles. |
| Phantom | 22 | Objet fantôme. |
| Radical | 23 | Objet radical, composé d'un radical, d'un élément de base et d'un degré optionnel. |
| SubscriptPart | 24 | Indice de l'objet pouvant avoir une partie d'indice. |
| SuperscriptPart | 25 | Exposant de l'objet exposant. |
| PreSubSuperscript | 26 | Objet pré-indice-exposant, qui se compose d'un élément de base ainsi que d'un indice et d'un exposant placés à gauche de la base. |
| Subscript | 27 | Objet indice, qui se compose d'un élément de base et d'un script de taille réduite placé en dessous et à droite. |
| SubSuperscript | 28 | Objet indice-exposant, qui se compose d'un élément de base, d'un script de taille réduite placé en dessous et à droite, et d'un script de taille réduite placé au-dessus et à droite. |
| Superscript | 29 | Objet exposant, qui se compose d'un élément de base et d'un script de taille réduite placé au-dessus et à droite. |
| None | 30 | Le type d'objet n'est pas spécifié. |

## Voir aussi

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
