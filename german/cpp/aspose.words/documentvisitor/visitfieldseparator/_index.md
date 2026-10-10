---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator Methode"
linktitle: "VisitFieldSeparator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator Methode. Wird aufgerufen, wenn ein Feldtrennzeichen im Dokument in C++ gefunden wird."
type: docs
weight: 22000
url: /de/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Aufgerufen, wenn ein Feldtrennzeichen im Dokument gefunden wird.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\<Aspose::Words::Fields::FieldSeparator\> | Das Objekt, das besucht wird. |

### ReturnValue

Ein [VisitorAction](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.
## Hinweise


Das Feldtrennzeichen trennt den Feldcode vom Feldwert im Dokument. Beachten Sie, dass einige Felder nur einen Feldcode besitzen und kein Feldtrennzeichen bzw. keinen Feldwert haben.

Weitere Informationen finden Sie unter [VisitFieldStart()](../visitfieldstart/)

## Siehe auch

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
