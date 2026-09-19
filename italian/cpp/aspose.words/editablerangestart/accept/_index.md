---
title: "Aspose::Words::EditableRangeStart::Accept metodo"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::EditableRangeStart::Accept metodo. Accetta un visitatore in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/editablerangestart/accept/
---
## EditableRangeStart::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::EditableRangeStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitEditableRangeStart()](../../documentvisitor/visiteditablerangestart/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
