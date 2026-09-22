---
title: "Aspose::Words::Saving::HtmlVersion enum"
linktitle: "HtmlVersion"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlVersion enum. يشير إلى إصدار HTML المستخدم عند حفظ المستند إلى صيغ Html و Mhtml في C++."
type: docs
weight: 62000
url: /ar/cpp/aspose.words.saving/htmlversion/
---
## HtmlVersion enum


يشير إلى إصدار HTML المستخدم عند حفظ المستند إلى صيغ [Html](../../aspose.words/saveformat/) و [Mhtml](../../aspose.words/saveformat/).

```cpp
enum class HtmlVersion
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Xhtml | 0 | يحفظ المستند وفقًا لمعيار XHTML 1.0 Transitional. |
| Html5 | 1 | يحفظ المستند وفقًا لمعيار HTML 5. |


## أمثلة



يوضح كيفية حفظ مستند إلى إصدار محدد من HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html", options);

// ستحتوي مستندات HTML الخاصة بنا على اختلافات طفيفة لتكون متوافقة مع إصدارات HTML المختلفة.
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case Aspose::Words::Saving::HtmlVersion::Html5:
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;

    case Aspose::Words::Saving::HtmlVersion::Xhtml:
        ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;

}
```


يوضح كيفية عرض عنوان DOCTYPE عند تحويل المستندات إلى معيار Xhtml 1.0 الانتقالي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// سيتضمن مستندنا عنوان إعلان DOCTYPE فقط إذا قمنا بتعيين العلامة "ExportXhtmlTransitional" إلى "true".
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
