---
title: "Metodo Aspose::Words::SubDocument::Accept"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::SubDocument::Accept. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/subdocument/accept/
---
## SubDocument::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::SubDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà i nodi. |

### ReturnValue

Vero se tutti i nodi sono stati visitati; falso se [DocumentVisitor](../../documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.
## Note


Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama il metodo corrispondente su [DocumentVisitor](../../documentvisitor/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
