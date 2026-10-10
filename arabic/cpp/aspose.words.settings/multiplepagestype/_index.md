---
title: "تعداد Aspose::Words::Settings::MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Settings::MultiplePagesType. يحدد كيفية طباعة المستند في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


يحدد كيفية طباعة المستند.

```cpp
enum class MultiplePagesType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| عادي | 0 | طباعة عادية، دون تحديد صفحات متعددة. |
| MirrorMargins | 1 | يبدل الهوامش اليسرى واليمنى في الصفحات المتقابلة. |
| TwoPagesPerSheet | 2 | يطبع صفحتين لكل ورقة. |
| BookFoldPrinting | 3 | تحدد ما إذا كان سيتم طباعة المستند كطية كتاب. |
| BookFoldPrintingReverse | 4 | تحدد ما إذا كان سيتم طباعة المستند كطية كتاب عكسية. |
| Default | n/a | القيمة الافتراضية هي [Normal](./) |


## أمثلة



يوضح كيفية تكوين مستند يمكن طباعته كطية كتاب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// أدرج نصًا يمتد عبر 16 صفحة.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// قم بتكوين خاصية "PageSetup" للقسم الأول لطباعة المستند على شكل طية كتاب.
// عند طباعة هذا المستند على الوجهين، يمكننا أخذ الصفحات لتجميعها
// وطويها جميعًا من الوسط مرة واحدة. محتويات المستند ستترتب على شكل طية كتاب.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// يمكننا تحديد عدد الأوراق فقط بأضعاف 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
