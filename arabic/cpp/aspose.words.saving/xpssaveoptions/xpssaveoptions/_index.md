---
title: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions منشئ"
linktitle: "XpsSaveOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions منشئ. يهيئ نسخة جديدة من هذه الفئة يمكن استخدامها لحفظ مستند بتنسيق Xps في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


يهيئ نسخة جديدة من هذه الفئة يمكن استخدامها لحفظ مستند بتنسيق [Xps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## أمثلة



يوضح كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند XPS المحفوظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج عناوين يمكن أن تُستخدم كمدخلات جدول المحتويات للمستويات 1 و2 ثم 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Xps, saveOptions->get_SaveFormat());

// سيتضمن مستند XPS الناتج مخططًا، جدول محتويات يسرد العناوين في جسم المستند.
// النقر على إدخال في هذا المخطط سينقلك إلى موقع العنوان المقابل.
// عيّن الخاصية "HeadingsOutlineLevels" إلى "2" لاستبعاد جميع العناوين التي مستوياتها أعلى من 2 من المخطط.
// العناوين الأخيرة التي أدرجناها أعلاه لن تظهر.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## انظر أيضًا

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


يهيئ نسخة جديدة من هذه الفئة يمكن استخدامها لحفظ مستند بتنسيق [Xps](../../../aspose.words/saveformat/) أو [OpenXps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


## أمثلة



يعرض كيفية حفظ مستند بتنسيق XPS على شكل طيّ كتاب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// اضبط الخاصية "UseBookFoldPrintingSettings" إلى "true" لترتيب المحتويات
// في XPS الناتج بطريقة تساعدنا على استخدامها لإنشاء كتيّب.
// قم بتعيين الخاصية "UseBookFoldPrintingSettings" إلى "false" لعرض XPS بشكل طبيعي.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// إذا كنا نقوم بعرض المستند ككتيب، يجب علينا ضبط "MultiplePages"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// بمجرد طباعة هذا المستند، يمكننا تحويله إلى كتيّب عن طريق رص الصفحات.
// للخروج من الطابعة وطيّها في المنتصف.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## انظر أيضًا

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
