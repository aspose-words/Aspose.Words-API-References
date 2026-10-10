---
title: "Aspose::Words::Math::OfficeMath::Accept méthode"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Math::OfficeMath::Accept méthode. Accepte un visiteur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.math/officemath/accept/
---
## OfficeMath::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::Math::OfficeMath::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
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
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words for C++](../../../)
