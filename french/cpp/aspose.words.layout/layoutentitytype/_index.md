---
title: "Aspose::Words::Layout::LayoutEntityType enum"
linktitle: "LayoutEntityType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::LayoutEntityType enum. Types des entités de mise en page en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Types des entités de mise en page.

```cpp
enum class LayoutEntityType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | n/a | Valeur par défaut. |
| Page | n/a | Représente une page d'un document. La page peut contenir des entités enfants [Colonne](./), [En-têtePiedDePage](./) et [Commentaire](./). |
| Column | n/a | Représente une colonne de texte sur une page. La colonne peut avoir les mêmes entités enfants que [Cell](./), plus les entités [Footnote](./), [Endnote](./) et [NoteSeparator](./). |
| Row | n/a | Représente une ligne de tableau. La ligne peut avoir [Cell](./) comme entités enfants. |
| Cell | n/a | Représente une cellule de tableau. La cellule peut avoir [Line](./) et [Row](./) comme entités enfants. |
| Line | n/a | Représente une ligne de caractères de texte et d'objets en ligne. La ligne peut avoir des entités enfants [Span](./). |
| Span | n/a | Représente un ou plusieurs caractères dans une ligne. Cela inclut des caractères spéciaux tels que les marqueurs de début/fin de champ, les signets et les commentaires. Span ne peut pas avoir d'entités enfants. |
| Footnote | n/a | Représente un espace réservé pour le contenu de la note de bas de page. Footnote peut avoir [Note](./) entités enfants. |
| Endnote | n/a | Représente un espace réservé pour le contenu de la note de fin. Endnote peut avoir [Note](./) entités enfants. |
| Note | n/a | Représente un espace réservé pour le contenu de la note. Note peut avoir [Line](./) et [Row](./) entités enfants. |
| HeaderFooter | n/a | Représente un espace réservé pour le contenu d'en-tête/pied de page sur une page. [HeaderFooter](../../aspose.words/headerfooter/) peut avoir [Line](./) et [Row](./) entités enfants. |
| TextBox | n/a | Représente la zone de texte à l'intérieur d'une forme. Textbox peut avoir [Line](./) et [Row](./) entités enfants. |
| Comment | n/a | Représente un espace réservé pour le contenu du commentaire. [Comment](../../aspose.words/comment/) peut avoir [Line](./) et [Row](./) entités enfants. |
| NoteSeparator | n/a | Représente le séparateur de note de bas de page/fin de note. NoteSeparator peut avoir [Line](./) et [Row](./) entités enfants. |

## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
