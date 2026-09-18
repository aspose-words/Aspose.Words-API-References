---
title: "Aspose::Words::DocumentVisitor::VisitFieldStart Methode"
linktitle: "VisitFieldStart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentVisitor::VisitFieldStart Methode. Aufgerufen, wenn ein Feld im Dokument in C++ beginnt."
type: docs
weight: 23000
url: /de/cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Aufgerufen, wenn ein Feld im Dokument beginnt.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | Das Objekt, das besucht wird. |

### ReturnValue

Ein [VisitorAction](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.
## Hinweise


Ein Feld in einem Word-Dokument besteht aus einem Feldcode und einem Feldwert.

Zum Beispiel kann ein Feld, das eine Seitenzahl anzeigt, wie folgt dargestellt werden:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Das Feldtrennzeichen trennt den Feldcode vom Feldwert im Dokument. Beachten Sie, dass einige Felder nur einen Feldcode besitzen und kein Feldtrennzeichen bzw. keinen Feldwert haben.

[Fields](../../../aspose.words.fields/) can be nested.

## Siehe auch

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
