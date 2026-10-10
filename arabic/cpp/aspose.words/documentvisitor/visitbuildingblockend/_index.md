---
title: "طريقة Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd"
linktitle: "VisitBuildingBlockEnd"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd. يتم استدعاؤها عندما ينتهي تعداد كتلة بناء في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor::VisitBuildingBlockEnd method


يتم الاستدعاء عندما ينتهي تعداد كتلة بناء.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitBuildingBlockEnd(System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> block)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| كتلة | System::SharedPtr\<Aspose::Words::BuildingBlocks::BuildingBlock\> | الكائن الذي يتم زيارته. |

### ReturnValue

قيمة [VisitorAction](../../visitoraction/) التي تحدد كيفية متابعة التعداد.
## ملاحظات


ملاحظة: لا يتم زيارة عقدة كتلة بناء وأبناؤها عندما تنفذ زائرًا على [Document](../../document/). إذا كنت تريد تنفيذ زائر على كتلة بناء، تحتاج إلى تنفيذ الزائر على [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/) أو استدعاء [Accept()](../../../aspose.words.buildingblocks/buildingblock/accept/).

## انظر أيضًا

* Enum [VisitorAction](../../visitoraction/)
* Class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
