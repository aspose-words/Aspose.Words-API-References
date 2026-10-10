---
title: "تعداد Aspose::Words::SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::SectionLayoutMode. يحدد وضع التخطيط لقسم يسمح بتعريف سلوك شبكة المستند في C++."
type: docs
weight: 115000
url: /ar/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


يحدد وضع التخطيط لقسم يسمح بتعريف سلوك شبكة المستند.

```cpp
enum class SectionLayoutMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| افتراضي | 0 | يحدد أنه لا يجب تطبيق شبكة المستند على محتويات القسم المقابل في المستند. |
| شبكة | 1 | يحدد أن القسم المقابل يجب أن يحتوي على كل من الارتفاع الإضافي للسطر والمسافة بين الأحرف مضافة إلى كل سطر وحرف داخله للحفاظ على عدد محدد من الأسطر في الصفحة والأحرف في السطر. لن يتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة أثناء الكتابة. |
| LineGrid | 2 | يحدد أن القسم المقابل يجب أن يحتوي على ارتفاع سطر إضافي يضاف إلى كل سطر داخله للحفاظ على عدد الأسطر المحدد في الصفحة. |
| SnapToChars | 3 | يحدد أن القسم المقابل يجب أن يحتوي على كل من الارتفاع الإضافي للسطر والمسافة بين الأحرف مضافة إلى كل سطر وحرف داخله للحفاظ على عدد محدد من الأسطر في الصفحة والأحرف في السطر. سيتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة أثناء الكتابة. |


## أمثلة



يعرض كيفية تحديد قيمة لعدد الأحرف التي قد يحتويها كل سطر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتمكين التباعد، ثم استخدمه لتعيين عدد الأحرف لكل سطر في هذا القسم.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// عدد الأحرف يعتمد أيضًا على حجم الخط.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
