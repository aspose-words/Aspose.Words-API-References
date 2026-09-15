---
title: "Aspose::Words::PageSetup::get_RtlGutter طريقة"
linktitle: "get_RtlGutter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::PageSetup::get_RtlGutter طريقة. يحصل على أو يعيّن ما إذا كان Microsoft Word يستخدم الهوامش للقسم بناءً على لغة من اليمين إلى اليسار أو من اليسار إلى اليمين في C++."
type: docs
weight: 40000
url: /ar/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


إحضار أو تعيين ما إذا كان Microsoft Word يستخدم الفواصل للقسم بناءً على لغة من اليمين إلى اليسار أو من اليسار إلى اليمين.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
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

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
