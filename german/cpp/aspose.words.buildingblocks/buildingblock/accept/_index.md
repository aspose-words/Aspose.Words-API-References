---
title: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildingBlocks::BuildingBlock::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der die Knoten besuchen wird. |

### ReturnValue

Wahr, wenn alle Knoten besucht wurden; falsch, wenn [DocumentVisitor](../../../aspose.words/documentvisitor/) die Operation gestoppt hat, bevor alle Knoten besucht wurden.
## Hinweise


Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft die entsprechende Methode auf [DocumentVisitor](../../../aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

Ruft [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/) auf, dann ruft es [Accept()](../../../aspose.words/node/accept/) für alle untergeordneten Knoten dieses Bausteins auf, anschließend ruft es [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/) auf.

Hinweis: Ein Bausteinknoten und seine Kinder werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../../aspose.words/document/) ausführen. Wenn Sie einen Visitor über einen Baustein ausführen möchten, müssen Sie den Visitor über ein [GlossaryDocument](../../glossarydocument/) ausführen oder [Accept()](./) aufrufen.

## Siehe auch

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
