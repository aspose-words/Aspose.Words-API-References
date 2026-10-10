---
title: "Aspose::Words::Fields::FieldEnd::Accept‑metoden"
linktitle: "Accept"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldEnd::Accept‑metoden. Accepterar en besökare i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldend/accept/
---
## FieldEnd::Accept method


Accepterar en besökare.

```cpp
bool Aspose::Words::Fields::FieldEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| besökare | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | Besökaren som kommer att besöka noden. |

### ReturnValue

**False** if the visitor requested the enumeration to stop.
## Anmärkningar


Anropar [VisitFieldEnd()](../../../aspose.words/documentvisitor/visitfieldend/).

För mer information, se Visitor-designmönstret.

## Se även

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FieldEnd](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
