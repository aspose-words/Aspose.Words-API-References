---
title: "طريقة Aspose::Words::Document::get_LastSection"
linktitle: "get_LastSection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_LastSection. يحصل على القسم الأخير في المستند في C++."
type: docs
weight: 35000
url: /ar/cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


يحصل على القسم الأخير في المستند.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## أمثلة



يوضح كيفية إنشاء قسم جديد باستخدام مُنشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// يحتوي مستند فارغ على قسم واحد بشكل افتراضي،
// الذي يحتوي على عقد فرعية يمكننا تعديلها.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// استخدم مُنشئ المستند لإضافة نص إلى القسم الأول.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// أنشئ قسمًا ثانيًا بإدراج فاصل قسم.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// لكل قسم إعدادات تخطيط صفحة خاصة به.
// يمكننا تقسيم النص في القسم الثاني إلى عمودين.
// هذا لن يؤثر على النص في القسم الأول.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```

## انظر أيضًا

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
