---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation"
linktitle: "get_ExportLanguageInformation"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation. تحدد ما إذا كانت معلومات اللغة تُصدَّر إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


يحدد ما إذا كانت معلومات اللغة تُصدر إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## ملاحظات


عند ضبط هذه الخاصية على **true** تقوم Aspose.Words بإخراج سمة HTML **lang** على عناصر المستند التي تحدد اللغة. قد يكون ذلك ضروريًا للحفاظ على الدلالات المتعلقة باللغة.

## أمثلة



يوضح كيفية الحفاظ على معلومات اللغة عند الحفظ إلى .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم المُنشئ لكتابة النص مع تنسيقه في لغات محلية مختلفة.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// عند حفظ المستند كـ HTML، يمكننا تمرير كائن SaveOptions
// لإما الحفاظ على أو إهمال لغة كل نص منسق.
// إذا قمنا بضبط علم \"ExportLanguageInformation\" إلى \"true\",
// ستحتوي وثيقة HTML الناتجة على اللغات في سمات \"lang\" لعلامات <span>.
// إذا قمنا بضبط علم \"ExportLanguageInformation\" إلى \"false',
// النص في وثيقة HTML الناتجة لن يحتوي على أي معلومات عن اللغة.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
