---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept method"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept-Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der die Knoten besuchen wird. |

### ReturnValue

Wahr, wenn alle Knoten besucht wurden; falsch, wenn [DocumentVisitor](../../../aspose.words/documentvisitor/) die Operation gestoppt hat, bevor alle Knoten besucht wurden.
## Hinweise


Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft die entsprechende Methode auf [DocumentVisitor](../../../aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

Ruft [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/) auf, ruft dann [Accept()](../../../aspose.words/node/accept/) für alle Kindknoten dieses Knotens auf und ruft anschließend [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) am Ende auf.

Hinweis: Ein Glossar-Dokumentknoten und seine Kinder werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../../aspose.words/document/) ausführen. Wenn Sie einen Visitor über ein Glossar-Dokument ausführen möchten, müssen Sie [Accept()](./) aufrufen.

## Siehe auch

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
