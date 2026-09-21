---
title: "Aspose::Words::Section::Accept‑metod"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Section::Accept‑metod. Accepterar en besökare i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/section/accept/
---
## Section::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::Section::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noderna. |

### ReturnValue

Sant om alla noder besöktes; falskt om [DocumentVisitor](../../documentvisitor/) stoppade operationen innan alla noder besöktes.
## Anmärkningar


Enumererar över denna nod och alla dess barn. Varje nod anropar en motsvarande metod på [DocumentVisitor](../../documentvisitor/).

För mer information, se Visitor-designmönstret.

## Se även

* Class [DocumentVisitor](../../documentvisitor/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
