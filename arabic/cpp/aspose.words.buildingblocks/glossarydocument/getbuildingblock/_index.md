---
title: "طريقة Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock"
linktitle: "GetBuildingBlock"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock. تبحث عن كتلة بناء باستخدام المعرض والفئة والاسم المحددين في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument::GetBuildingBlock method


يبحث عن كتلة بناء باستخدام المعرض والفئة والاسم المحددين.

```cpp
System::SharedPtr<Aspose::Words::BuildingBlocks::BuildingBlock> Aspose::Words::BuildingBlocks::GlossaryDocument::GetBuildingBlock(Aspose::Words::BuildingBlocks::BuildingBlockGallery gallery, const System::String &category, const System::String &name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| معرض | Aspose::Words::BuildingBlocks::BuildingBlockGallery | معايير المعرض. |
| فئة | const System::String\& | معايير الفئة. يمكن أن تكون **null**، وفي هذه الحالة لن تُستخدم للمقارنة. |
| name | const System::String\& | معايير اسم كتلة البناء. |

### ReturnValue

كتلة البناء المتطابقة أو **null** إذا لم يتم العثور على تطابق.
## ملاحظات


هذه طريقة ملائمة تُعيد جميع كتل البناء في هذه المجموعة وتُرجع أول كتلة بناء تتطابق مع المعرض والفئة والاسم المحددين.

يقوم Microsoft Word بتنظيم كتل البناء في معارض. تُعرّف المعارض مسبقًا باستخدام تعداد [BuildingBlockGallery](../../buildingblockgallery/). داخل كل معرض، يمكن تنظيم كتل البناء في فئة واحدة أو أكثر. اسم الفئة هو سلسلة نصية. كل كتلة بناء لها اسم. لا يُضمن أن يكون اسم كتلة البناء فريدًا.

## انظر أيضًا

* Class [BuildingBlock](../../buildingblock/)
* Enum [BuildingBlockGallery](../../buildingblockgallery/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
