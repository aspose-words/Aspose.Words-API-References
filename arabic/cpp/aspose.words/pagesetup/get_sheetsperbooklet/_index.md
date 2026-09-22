---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet طريقة"
linktitle: "get_SheetsPerBooklet"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet طريقة. تُرجع أو تُعيّن عدد الصفحات التي تُدرج في كل كتيب في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


إرجاع أو تعيين عدد الصفحات التي سيتم تضمينها في كل كتيب.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
