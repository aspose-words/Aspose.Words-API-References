---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTagRangeEnd::Accept"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTagRangeEnd::Accept. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTagRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà i nodi. |

### ReturnValue

Vero se tutti i nodi sono stati visitati; falso se [DocumentVisitor](../../../aspose.words/documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.
## Note


Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama il metodo corrispondente su [DocumentVisitor](../../../aspose.words/documentvisitor/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [StructuredDocumentTagRangeEnd](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
