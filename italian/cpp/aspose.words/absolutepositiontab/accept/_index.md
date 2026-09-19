---
title: "Aspose::Words::AbsolutePositionTab::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::AbsolutePositionTab::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
