---
title: "Aspose::Words::Body::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Body::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/body/accept/
---
## Body::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::Body::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
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
* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
