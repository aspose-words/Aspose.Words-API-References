---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà i nodi. |

### ReturnValue

Vero se tutti i nodi sono stati visitati; falso se [DocumentVisitor](../../../aspose.words/documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.
## Note


Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama il metodo corrispondente su [DocumentVisitor](../../../aspose.words/documentvisitor/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

Chiama [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/), poi chiama [Accept()](../../../aspose.words/node/accept/) per tutti i nodi figli di questo nodo e infine chiama [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) alla fine.

Nota: Un nodo di documento glossary e i suoi figli non vengono visitati quando esegui un Visitor su un [Document](../../../aspose.words/document/). Se vuoi eseguire un Visitor su un documento glossary, devi chiamare [Accept()](./).

## Vedi anche

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
