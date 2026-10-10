---
title: "طريقة Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart"
linktitle: "VisitGlossaryDocumentStart"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart. تُستدعى عندما يبدأ تعداد مستند القاموس في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


يتم استدعاؤه عندما يبدأ تعداد مستند المسرد.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
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
