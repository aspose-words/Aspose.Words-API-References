---
title: "Aspose::Words::BookmarkStart::Accept méthode"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BookmarkStart::Accept méthode. Accepte un visiteur en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/bookmarkstart/accept/
---
## BookmarkStart::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::BookmarkStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui visitera le nœud. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarques


Appelle [VisitBookmarkStart()](../../documentvisitor/visitbookmarkstart/).

Pour plus d'informations, consultez le modèle de conception Visitor.

## Voir aussi

* Class [DocumentVisitor](../../documentvisitor/)
* Class [BookmarkStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
