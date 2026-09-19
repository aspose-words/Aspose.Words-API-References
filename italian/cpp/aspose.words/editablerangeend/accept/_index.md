---
title: "Metodo Aspose::Words::EditableRangeEnd::Accept"
linktitle: "Accept"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::EditableRangeEnd::Accept. Accetta un visitor in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


Accetta un visitatore.

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitatore | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Il visitatore che visiterà il nodo. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Note


Chiama [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/).

Per ulteriori informazioni vedere il pattern di progettazione Visitor.

## Vedi anche

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
