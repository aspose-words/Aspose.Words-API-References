---
title: "طريقة Aspose::Words::PageSetup::get_Gutter"
linktitle: "get_Gutter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_Gutter. يحصل على أو يضبط مقدار المسافة الإضافية المضافة إلى الهامش لتجليد المستند في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words/pagesetup/get_gutter/
---
## PageSetup::get_Gutter method


يحصل أو يعيّن مقدار المسافة الإضافية المضافة إلى الهامش لتثبيت المستند.

```cpp
double Aspose::Words::PageSetup::get_Gutter()
```


## أمثلة



يظهر كيفية تعيين هوامش الفجوة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إدراج نص يمتد عبر عدة صفحات.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// تضيف الفجوة مساحات بيضاء إما إلى الهامش الأيسر أو الأيمن للصفحة،
// مما يعوض عن طيّ الصفحات في وسط الكتاب الذي يقتحم تخطيط الصفحة.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// حدد مقدار المساحة المتاحة للنص داخل هوامش الصفحات ثم أضف مقدارًا لتوسيع الهامش.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// عيّن الخاصية \"RtlGutter\" إلى \"true\" لوضع الفجوة في موقع أكثر ملاءمة للنص من اليمين إلى اليسار.
pageSetup->set_RtlGutter(true);

// عيّن الخاصية \"MultiplePages\" إلى \"MultiplePagesType.MirrorMargins\" لتبديل
// موضع هوامش الجانب الأيسر/الأيمن لكل صفحة.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```


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
