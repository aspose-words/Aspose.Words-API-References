---
title: Aspose::Words::DocumentVisitor::VisitFieldStart method
linktitle: VisitFieldStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitFieldStart method. Called when a field starts in the document in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor::VisitFieldStart method


Called when a field starts in the document.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldStart(System::SharedPtr<Aspose::Words::Fields::FieldStart> fieldStart)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldStart | System::SharedPtr\<Aspose::Words::Fields::FieldStart\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.
## Remarks


A field in a Word document consists of a field code and field value.

For example, a field that displays a page number can be represented as follows:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

The field separator separates field code from field value in the document. Note that some fields have only field code and do not have field separator and field value.

[Fields](../../../aspose.words.fields/) can be nested.

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldStart](../../../aspose.words.fields/fieldstart/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
