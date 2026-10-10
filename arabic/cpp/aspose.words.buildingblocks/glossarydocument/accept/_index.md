---
title: "طريقة Aspose::Words::BuildingBlocks::GlossaryDocument::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BuildingBlocks::GlossaryDocument::Accept. تقبل زائرًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقد. |

### ReturnValue

صحيح إذا تم زيارة جميع العقد؛ خطأ إذا أوقف [DocumentVisitor](../../../aspose.words/documentvisitor/) العملية قبل زيارة جميع العقد.
## ملاحظات


يعدّ هذا العقد وجميع أبنائه. كل عقدة تستدعي الطريقة المقابلة على [DocumentVisitor](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

تستدعي [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/)، ثم تستدعي [Accept()](../../../aspose.words/node/accept/) لجميع العقد الفرعية لهذه العقدة ثم تستدعي [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/) في النهاية.

ملاحظة: لا يتم زيارة عقدة مستند القاموس وأطفالها عند تنفيذ زائر على [Document](../../../aspose.words/document/). إذا كنت تريد تنفيذ زائر على مستند القاموس، تحتاج إلى استدعاء [Accept()](./).

## انظر أيضًا

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
