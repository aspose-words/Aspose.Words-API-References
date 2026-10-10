---
title: "Aspose::Words::PageSetup::get_CharactersPerLine method"
linktitle: "get_CharactersPerLine"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_CharactersPerLine method. يحصل على أو يضبط عدد الأحرف في السطر في شبكة المستند في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


يحصل أو يعيّن عدد الأحرف في كل سطر في شبكة المستند.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## ملاحظات


القيمة الدنيا للخاصية هي 1. القيمة القصوى تعتمد على عرض الصفحة وحجم الخط للنمط العادي. الحد الأدنى لتباعد الأحرف هو 90٪ من حجم الخط. على سبيل المثال، الحد الأقصى لعدد الأحرف في السطر لصفحة بحجم Letter مع هوامش بوصة واحدة هو 43.

بشكل افتراضي، تحتوي الخاصية على قيمة يكون فيها تباعد الأحرف مساويًا لحجم الخط للنمط العادي.

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

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
