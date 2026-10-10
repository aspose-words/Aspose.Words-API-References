---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator metod"
linktitle: "VisitFieldSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator metod. Anropas när ett fältseparator påträffas i dokumentet i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Kallas när en fältseparator påträffas i dokumentet.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | Objektet som besöks. |

### ReturnValue

Ett [VisitorAction](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.
## Anmärkningar


Fältseparatorn separerar fältkod från fältvärde i dokumentet. Observera att vissa fält endast har fältkod och saknar fältseparator och fältvärde.

För mer information, se [VisitFieldStart()](../visitfieldstart/)

## Se även

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
