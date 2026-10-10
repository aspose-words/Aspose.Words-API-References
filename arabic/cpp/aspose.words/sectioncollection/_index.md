---
title: "Aspose::Words::SectionCollection فئة"
linktitle: "SectionCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::SectionCollection class. مجموعة من كائنات Section في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 59000
url: /ar/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


مجموعة من كائنات [Section](../section/) في المستند. لمعرفة المزيد، زر مقالة الوثائق [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get_Count](../nodecollection/get_count/)() | يحصل على عدد العقد في المجموعة. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يسترجع section عند الفهرس المحدد. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يعيد الفهرس الصفري للعقدة المحددة. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](./toarray/)() | ينسخ جميع sections من المجموعة إلى مصفوفة جديدة من sections. |
| static [Type](./type/)() |  |
## ملاحظات


يمكن لمستند Microsoft Word أن يحتوي على أقسام متعددة. لإنشاء قسم في Microsoft Word، اختر أمر Insert/Break وحدد نوع الفاصل. يحدد الفاصل ما إذا كان القسم يبدأ في صفحة جديدة أو في نفس الصفحة.

يمكن استخدام إدراج وإزالة الأقسام برمجيًا لتخصيص المستندات التي تُنتج أثناء دمج البريد. إذا كان المستند يحتاج إلى محتوى مختلف أو أجزاء من المحتوى بناءً على معايير معينة، يمكنك إنشاء مستند "master" يحتوي على أقسام متعددة وحذف بعض الأقسام قبل أو بعد دمج البريد.

## أمثلة



يوضح كيفية إضافة وإزالة الأقسام في مستند
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// احذف القسم الأول من المستند
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// أضف نسخة من ما هو الآن القسم الأول إلى نهاية المستند
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## انظر أيضًا

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
