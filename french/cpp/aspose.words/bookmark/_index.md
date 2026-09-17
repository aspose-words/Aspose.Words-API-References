---
title: "Aspose::Words::Bookmark classe"
linktitle: "Signet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Bookmark classe. Représente un seul signet. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/bookmark/
---
## Bookmark class


Représente un signet unique. Pour en savoir plus, consultez l'article de documentation [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class Bookmark : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Obtient le nœud qui représente la fin du signet. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Obtient le nœud qui représente le début du signet. |
| [get_FirstColumn](./get_firstcolumn/)() | Obtient l'index basé sur zéro de la première colonne de la plage de colonnes du tableau associée au signet. |
| [get_IsColumn](./get_iscolumn/)() | Renvoie **true** si ce signet est un signet de colonne de tableau. |
| [get_LastColumn](./get_lastcolumn/)() | Obtient l'index basé sur zéro de la dernière colonne de la plage de colonnes du tableau associée au signet. |
| [get_Name](./get_name/)() | Obtient ou définit le nom du signet. |
| [get_Text](./get_text/)() | Obtient le texte contenu dans le signet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime le signet du document. Ne supprime pas le texte à l'intérieur du signet. |
| [set_Name](./set_name/)(const System::String\&) | Mutateur pour [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Définit le texte contenu dans le signet. |
| static [Type](./type/)() |  |
## Remarques


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
