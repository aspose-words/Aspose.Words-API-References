---
title: "طريقة Aspose::Words::ParagraphFormat::get_SnapToGrid"
linktitle: "get_SnapToGrid"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_SnapToGrid. تحدد ما إذا كان الفقرة الحالية يجب أن تستخدم إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتويات في الفقرة في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


يحدد ما إذا كان يجب على الفقرة الحالية استخدام إعدادات خطوط شبكة المستند لكل صفحة عند تنسيق المحتوى في الفقرة.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


## أمثلة



يوضح كيفية تحديد حد لعدد الأسطر التي قد يحتويها كل صفحة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتمكين التباعد، ثم استخدمه لتعيين عدد الأسطر لكل صفحة في هذا القسم.
// حجم خط كبير بما فيه الكفاية سيدفع بعض الأسطر إلى الصفحة التالية لتجنب تداخل الأحرف.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
