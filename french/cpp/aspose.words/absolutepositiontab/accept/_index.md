---
title: "Aspose::Words::AbsolutePositionTab::Accept méthode"
linktitle: "Accept"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::AbsolutePositionTab::Accept méthode. Accepte un visiteur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Accepte un visiteur.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| visiteur | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Le visiteur qui visitera le nœud. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarques


Appelle [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

Pour plus d'informations, consultez le modèle de conception Visitor.

## Voir aussi

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
