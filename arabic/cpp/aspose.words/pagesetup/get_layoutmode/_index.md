---
title: "طريقة Aspose::Words::PageSetup::get_LayoutMode"
linktitle: "get_LayoutMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_LayoutMode. يحصل على أو يضبط وضع التخطيط لهذا القسم في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words/pagesetup/get_layoutmode/
---
## PageSetup::get_LayoutMode method


يحصل أو يعيّن وضع التخطيط لهذا القسم.

```cpp
Aspose::Words::SectionLayoutMode Aspose::Words::PageSetup::get_LayoutMode()
```


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

* Enum [SectionLayoutMode](../../sectionlayoutmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
