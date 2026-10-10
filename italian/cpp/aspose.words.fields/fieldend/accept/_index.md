---
title: "Aspose::Words::Fields::FieldEnd::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldEnd::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldend/accept/
---
## FieldEnd::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::Fields::FieldEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitFieldEnd()](../../../aspose.words/documentvisitor/visitfieldend/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldEnd](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
