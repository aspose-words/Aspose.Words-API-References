---
title: "Aspose::Words::EditableRangeEnd::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::EditableRangeEnd::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/editablerangeend/accept/
---
## EditableRangeEnd::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::EditableRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der den Knoten besuchen wird. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Hinweise


Ruft [VisitEditableRangeEnd()](../../documentvisitor/visiteditablerangeend/) auf.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

## Siehe auch

* Class [DocumentVisitor](../../documentvisitor/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
