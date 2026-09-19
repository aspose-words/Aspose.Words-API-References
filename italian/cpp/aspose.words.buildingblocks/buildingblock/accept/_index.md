---
title: "Metodo Accept di Aspose::Words::BuildingBlocks::BuildingBlock"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Accept di Aspose::Words::BuildingBlocks::BuildingBlock. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà i nodi. |

### ReturnValue

Vero se tutti i nodi sono stati visitati; falso se [DocumentVisitor](../../../aspose.words/documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.
## Note


Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama il metodo corrispondente su [DocumentVisitor](../../../aspose.words/documentvisitor/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

Chiama [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/), quindi chiama [Accept()](../../../aspose.words/node/accept/) per tutti i nodi figli di questo blocco di costruzione, quindi chiama [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Nota: Un nodo di blocco di costruzione e i suoi figli non vengono visitati quando si esegue un Visitor su un [Document](../../../aspose.words/document/). Se si desidera eseguire un Visitor su un blocco di costruzione, è necessario eseguire il visitor su [GlossaryDocument](../../glossarydocument/) o chiamare [Accept()](./).

## Vedi anche

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
