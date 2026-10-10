---
title: "Metodo Aspose::Words::Fields::FieldSeparator::Accept"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldSeparator::Accept. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldseparator/accept/
---
## FieldSeparator::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::Fields::FieldSeparator::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitFieldSeparator()](../../../aspose.words/documentvisitor/visitfieldseparator/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldSeparator](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
