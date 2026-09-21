---
title: "Aspose::Words::Fields::FieldStart::Accept-metoden"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldStart::Accept-metoden. Accepterar en besökare i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldstart/accept/
---
## FieldStart::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::Fields::FieldStart::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noden. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Anmärkningar


Anropar [VisitFieldStart()](../../../aspose.words/documentvisitor/visitfieldstart/).

För mer information, se Visitor-designmönstret.

## Se även

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
