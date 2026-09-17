---
title: "Méthode Accept de Aspose::Words::Tables::Cell"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Accept de Aspose::Words::Tables::Cell. Accepte un visiteur en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.tables/cell/accept/
---
## Cell::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::Tables::Cell::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui parcourra les nœuds. |

### ReturnValue

Vrai si tous les nœuds ont été parcourus ; faux si [DocumentVisitor](../../../aspose.words/documentvisitor/) a interrompu l'opération avant de parcourir tous les nœuds.
## Remarques


Énumère ce nœud et tous ses enfants. Chaque nœud appelle une méthode correspondante sur [DocumentVisitor](../../../aspose.words/documentvisitor/).

Pour plus d'informations, consultez le modèle de conception Visitor.

## Voir aussi

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
