---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart méthode"
linktitle: "VisitBuildingBlockStart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart méthode. Appelée lorsque l'énumération d'un bloc de construction a commencé en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor::VisitBuildingBlockStart method


Appelé lorsque l'énumération d'un bloc de construction a commencé.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockStart(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bloc | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | L'objet qui est visité. |

### ReturnValue

Une valeur [VisitorAction](../../visitoraction/) qui spécifie comment poursuivre l'énumération.
## Remarques


Remarque : Un nœud de bloc de construction et ses enfants ne sont pas parcourus lorsque vous exécutez un Visitor sur un [Document](../../document/). Si vous souhaitez exécuter un Visitor sur un bloc de construction, vous devez exécuter le visiteur sur un [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) ou appeler [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## Voir aussi

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
