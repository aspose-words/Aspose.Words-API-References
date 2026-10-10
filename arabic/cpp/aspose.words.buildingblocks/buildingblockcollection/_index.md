---
title: "فئة Aspose::Words::BuildingBlocks::BuildingBlockCollection"
linktitle: "BuildingBlockCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::BuildingBlocks::BuildingBlockCollection. مجموعة من كائنات BuildingBlock في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class


مجموعة من كائنات [BuildingBlock](../buildingblock/) في المستند. لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlockCollection : public Aspose::Words::NodeCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | يحصل على عدد العقد في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يسترجع كتلة بناء عند الفهرس المحدد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](./toarray/)() | ينسخ جميع كتل البناء من المجموعة إلى مصفوفة جديدة من كتل البناء. |
| static [Type](./type/)() |  |
## ملاحظات


أنت لا تنشئ مثيلات من هذه الفئة مباشرة. للوصول إلى مجموعة من كتل البناء استخدم خاصية [BuildingBlocks](../glossarydocument/get_buildingblocks/).

## انظر أيضًا

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
