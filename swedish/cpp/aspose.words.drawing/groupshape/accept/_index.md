---
title: "Aspose::Words::Drawing::GroupShape::Accept‑metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::GroupShape::Accept‑metod. Accepterar en besökare i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/groupshape/accept/
---
## GroupShape::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::Drawing::GroupShape::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
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
* Class [GroupShape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
