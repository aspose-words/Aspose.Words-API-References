---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart metod"
linktitle: "VisitFieldStart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart metod. Anropas när ett fält startar i dokumentet i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Kallas när ett fält startar i dokumentet.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | Objektet som besöks. |

### ReturnValue

Ett [VisitorAction](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.
## Anmärkningar


Ett feld i ett Word-dokument består av en fältkod och ett fältvärde.

Till exempel kan ett fält som visar ett sidnummer representeras på följande sätt:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Fältseparatorn separerar fältkod från fältvärde i dokumentet. Observera att vissa fält endast har fältkod och saknar fältseparator och fältvärde.

[Fields](../../../aspose.words.fields/) can be nested.

## Se även

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
