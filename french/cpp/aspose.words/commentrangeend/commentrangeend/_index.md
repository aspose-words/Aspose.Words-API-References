---
title: "Aspose::Words::CommentRangeEnd::CommentRangeEnd constructeur"
linktitle: "CommentRangeEnd"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CommentRangeEnd::CommentRangeEnd constructeur. Initialise une nouvelle instance de cette classe en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/commentrangeend/commentrangeend/
---
## CommentRangeEnd::CommentRangeEnd constructor


Initialise une nouvelle instance de cette classe.

```cpp
Aspose::Words::CommentRangeEnd::CommentRangeEnd(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, int32_t id)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
| id | int32_t | L'identifiant du commentaire auquel cet objet est lié. |
## Remarques


Lorsque [CommentRangeEnd](../) est créé, il appartient au document spécifié, mais ne fait pas encore partie du document et [ParentNode](../../node/get_parentnode/) est **null**.

Pour ajouter un [CommentRangeEnd](../) au document, utilisez InsertAfter ou InsertBefore sur le paragraphe où vous souhaitez insérer le commentaire.

## Voir aussi

* Class [DocumentBase](../../documentbase/)
* Class [CommentRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
