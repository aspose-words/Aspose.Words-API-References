---
title: "Aspose::Words::AbsolutePositionTab::Accept Methode"
linktitle: "Accept"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AbsolutePositionTab::Accept Methode. Akzeptiert einen Besucher in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Akzeptiert einen Besucher.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Besucher | System::SharedPtr\\<Aspose::Words::DocumentVisitor\\> | Der Besucher, der den Knoten besuchen wird. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Hinweise


Ruft [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/) auf.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

## Siehe auch

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
