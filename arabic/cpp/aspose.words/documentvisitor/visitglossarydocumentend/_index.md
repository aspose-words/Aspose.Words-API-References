---
title: "طريقة Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd"
linktitle: "VisitGlossaryDocumentEnd"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd. يتم استدعاؤها عندما ينتهي تعداد مستند مسرد في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words/documentvisitor/visitglossarydocumentend/
---
## DocumentVisitor::VisitGlossaryDocumentEnd method


يتم استدعاؤه عندما ينتهي تعداد مستند المسرد.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| glossary | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | الكائن الذي يتم زيارته. |

### ReturnValue

قيمة [VisitorAction](../../visitoraction/) التي تحدد كيفية متابعة التعداد.
## ملاحظات


ملاحظة: لا يتم زيارة عقدة مستند القاموس وأبنائها عند تنفيذ زائر على [Document](../../document/). إذا كنت تريد تنفيذ زائر على مستند القاموس، تحتاج إلى استدعاء [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/).

## انظر أيضًا

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
