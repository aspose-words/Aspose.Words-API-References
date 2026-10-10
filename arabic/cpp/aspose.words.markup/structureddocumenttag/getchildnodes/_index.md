---
title: "طريقة Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes"
linktitle: "GetChildNodes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes. تُرجع مجموعة حية من العقد الفرعية التي تطابق النوع المحدد في C++."
type: docs
weight: 34500
url: /ar/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | يحدد نوع العقد التي سيتم اختيارها. |
| isDeep | bool | **true** لتحديد جميع العقد الفرعية بشكل متكرر؛ **false** لتحديد فقط بين الأطفال المباشرين. |

### ReturnValue

مجموعة حية من العقد الفرعية من النوع المحدد.
## ملاحظات


المجموعة التي تُرجعها هذه الطريقة دائمًا حية.

المجموعة الحية تكون دائمًا متزامنة مع المستند. على سبيل المثال، إذا قمت بتحديد جميع الأقسام في مستند وتقوم بالتعداد عبر المجموعة بحذف الأقسام، يتم إزالة القسم من المجموعة فورًا عندما يُحذف من المستند.

## انظر أيضًا

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
