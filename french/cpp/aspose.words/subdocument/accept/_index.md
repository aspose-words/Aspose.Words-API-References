---
title: "Aspose::Words::SubDocument::Accept méthode"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::SubDocument::Accept méthode. Accepte un visiteur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/subdocument/accept/
---
## SubDocument::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::SubDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui parcourra les nœuds. |

### ReturnValue

Vrai si tous les nœuds ont été visités ; faux si [DocumentVisitor](../../documentvisitor/) a interrompu l'opération avant de visiter tous les nœuds.
## Remarques


Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur [DocumentVisitor](../../documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

## Voir aussi

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
