---
title: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart metodo"
linktitle: "VisitBuildingBlockStart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentVisitor::VisitBuildingBlockStart metodo. Chiamato quando l'enumerazione di un blocco di costruzione è iniziata in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor::VisitBuildingBlockStart method


Chiamato quando l'enumerazione di un blocco di costruzione è iniziata.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockStart(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| blocco | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | L'oggetto che viene visitato. |

### ReturnValue

Un valore [VisitorAction](../../visitoraction/) che specifica come continuare l'enumerazione.
## Note


Nota: Un nodo di blocco di costruzione e i suoi figli non vengono visitati quando si esegue un Visitor su un [Document](../../document/). Se si desidera eseguire un Visitor su un blocco di costruzione, è necessario eseguire il visitor su [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) o chiamare [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## Vedi anche

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
