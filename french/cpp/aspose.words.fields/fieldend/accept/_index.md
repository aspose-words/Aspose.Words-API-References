---
title: "Méthode Aspose::Words::Fields::FieldEnd::Accept"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FieldEnd::Accept. Accepte un visiteur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldend/accept/
---
## FieldEnd::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::Fields::FieldEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui visitera le nœud. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Remarques


Appelle [VisitFieldEnd()](../../../aspose.words/documentvisitor/visitfieldend/).

Pour plus d'informations, consultez le modèle de conception Visitor.

## Voir aussi

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldEnd](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
