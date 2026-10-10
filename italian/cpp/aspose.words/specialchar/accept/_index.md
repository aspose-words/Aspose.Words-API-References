---
title: "Aspose::Words::SpecialChar::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::SpecialChar::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/specialchar/accept/
---
## SpecialChar::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::SpecialChar::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitSpecialChar()](../../documentvisitor/visitspecialchar/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [SpecialChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
