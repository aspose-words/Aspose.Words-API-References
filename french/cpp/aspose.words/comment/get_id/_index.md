---
title: "Aspose::Words::Comment::get_Id méthode"
linktitle: "get_Id"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment::get_Id méthode. Obtient ou définit l'identifiant du commentaire en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/comment/get_id/
---
## Comment::get_Id method


Obtient ou définit l'identifiant du commentaire.

```cpp
int32_t Aspose::Words::Comment::get_Id() const
```

## Remarques


L'identifiant du commentaire permet d'ancrer un commentaire à une région de texte dans le document. La région doit être délimitée à l'aide des objets [CommentRangeStart](../../commentrangestart/) et [CommentRangeEnd](../../commentrangeend/) partageant la même valeur d'identifiant que l'objet [Comment](../).

Vous utiliseriez cette valeur lors de la recherche des nœuds [CommentRangeStart](../../commentrangestart/) et [CommentRangeEnd](../../commentrangeend/) liés à ce commentaire.

[Comment](../) identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents. 
## Voir aussi

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
