---
title: "Aspose::Words::Tables::Cell::Accept‑metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Cell::Accept‑metod. Accepterar en besökare i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.tables/cell/accept/
---
## Cell::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::Tables::Cell::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noderna. |

### ReturnValue

Sant om alla noder har besökts; falskt om [DocumentVisitor](../../../aspose.words/documentvisitor/) stoppade operationen innan alla noder besöktes.
## Anmärkningar


Enumererar denna nod och alla dess barn. Varje nod anropar en motsvarande metod på [DocumentVisitor](../../../aspose.words/documentvisitor/).

För mer information, se Visitor-designmönstret.

## Se även

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
