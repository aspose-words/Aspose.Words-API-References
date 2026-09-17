---
title: "Aspose::Words::CommentRangeStart::Accept méthode"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CommentRangeStart::Accept méthode. Accepte un visiteur en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/commentrangestart/accept/
---
## CommentRangeStart::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::CommentRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui visitera le nœud. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarques


Appelle [VisitCommentRangeStart()](../../documentvisitor/visitcommentrangestart/).

Pour plus d'informations, consultez le modèle de conception Visitor.

## Voir aussi

* Class [DocumentVisitor](../../documentvisitor/)
* Class [CommentRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
