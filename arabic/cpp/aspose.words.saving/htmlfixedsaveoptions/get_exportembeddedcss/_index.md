---
title: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss"
linktitle: "get_ExportEmbeddedCss"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss. تحدد ما إذا كان يجب تضمين CSS (Cascading Style Sheet) في مستند Html في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


تحدد ما إذا كان يجب تضمين CSS (Cascading [Style](../../../aspose.words/style/) Sheet) في مستند Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## أمثلة



يوضح كيفية تحديد مكان تخزين أوراق أنماط CSS عند تصدير مستند إلى Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// عند تصديرنا مستندًا إلى html، سيقوم Aspose.Words أيضًا بإنشاء ورقة أنماط CSS لتنسيق المستند.
// ضبط العلامة "ExportEmbeddedCss" إلى "true" يحفظ ورقة أنماط CSS في ملف .css،
// ويربط بالملف من مستند html باستخدام عنصر <link>.
// ضبط العلامة إلى "false" سيضمن ورقة أنماط CSS داخل مستند Html،
// مما سيؤدي إلى إنشاء ملف واحد فقط بدلاً من ملفين.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
