---
title: "طريقة Aspose::Words::BuildingBlocks::BuildingBlock::Accept"
linktitle: "Accept"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BuildingBlocks::BuildingBlock::Accept. تقبل زائرًا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock::Accept method


يقبل زائرًا.

```cpp
bool Aspose::Words::BuildingBlocks::BuildingBlock::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| زائر | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | الزائر الذي سيزور العقد. |

### ReturnValue

صحيح إذا تم زيارة جميع العقد؛ خطأ إذا أوقف [DocumentVisitor](../../../aspose.words/documentvisitor/) العملية قبل زيارة جميع العقد.
## ملاحظات


يعدّ هذا العقد وجميع أبنائه. كل عقدة تستدعي الطريقة المقابلة على [DocumentVisitor](../../../aspose.words/documentvisitor/).

لمزيد من المعلومات راجع نمط التصميم Visitor.

ينادي [VisitBuildingBlockStart()](../../../aspose.words/documentvisitor/visitbuildingblockstart/)، ثم ينادي [Accept()](../../../aspose.words/node/accept/) لجميع العقد الفرعية لهذه كتلة البناء، ثم ينادي [VisitBuildingBlockEnd()](../../../aspose.words/documentvisitor/visitbuildingblockend/).

ملاحظة: لا يتم زيارة عقدة كتلة البناء وأطفالها عندما تقوم بتنفيذ Visitor على [Document](../../../aspose.words/document/). إذا كنت ترغب في تنفيذ Visitor على كتلة بناء، تحتاج إلى تنفيذ الزائر على [GlossaryDocument](../../glossarydocument/) أو استدعاء [Accept()](./).

## انظر أيضًا

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [BuildingBlock](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
