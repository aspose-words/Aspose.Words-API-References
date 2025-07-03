---
title: Aspose::Words::Fields::FormField::Accept method
linktitle: Accept
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FormField::Accept method. Accepts a visitor in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fields/formfield/accept/
---
## FormField::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::Fields::FormField::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitFormField()](../../../aspose.words/documentvisitor/visitformfield/).

For more info see the Visitor design pattern.

## See Also

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
