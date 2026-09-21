---
title: "Aspose::Words::AbsolutePositionTab::Accept metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AbsolutePositionTab::Accept metod. Accepterar en besökare i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noden. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Anmärkningar


Anropar [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

För mer information, se Visitor-designmönstret.

## Se även

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
