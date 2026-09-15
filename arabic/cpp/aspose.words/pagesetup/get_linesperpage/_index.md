---
title: "طريقة Aspose::Words::PageSetup::get_LinesPerPage"
linktitle: "get_LinesPerPage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_LinesPerPage. تحصّل أو تعيين عدد الأسطر في الصفحة في شبكة المستند في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


يحصل أو يعيّن عدد الأسطر في كل صفحة في شبكة المستند.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## ملاحظات


القيمة الدنيا للخاصية هي 1. القيمة القصوى تعتمد على ارتفاع الصفحة وحجم الخط للنمط العادي. الحد الأدنى لتباعد الأسطر هو 136٪ من حجم الخط. على سبيل المثال، الحد الأقصى لعدد الأسطر في الصفحة لصفحة بحجم Letter مع هوامش بوصة واحدة هو 39.

بشكل افتراضي، تحتوي الخاصية على قيمة يكون فيها تباعد الأسطر أكبر بمقدار 1.5 مرة من حجم الخط للنمط العادي.

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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
