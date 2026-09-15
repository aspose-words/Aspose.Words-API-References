---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg طريقة"
linktitle: "get_ExportEmbeddedSvg"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg طريقة. يحدد ما إذا كان يجب تضمين موارد SVG في مستند Html. القيمة الافتراضية هي true في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


يحدد ما إذا كان يجب تضمين موارد SVG في مستند Html. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## أمثلة



يوضح كيفية تحديد مكان تخزين كائنات SVG عند تصدير مستند إلى Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// عند تصدير مستند يحتوي على كائنات SVG إلى .html،
// يمكن لـ Aspose.Words وضع هذه الكائنات في موقعين محتملين.
// ضبط علم "ExportEmbeddedSvg" إلى "true" سيؤدي إلى تضمين جميع بيانات SVG الخام
// داخل HTML الناتج، داخل وسوم <image>.
// ضبط هذا العلم إلى "false" سيؤدي إلى إنشاء ملف في نظام الملفات المحلي لكل كائن SVG.
// سيرتبط HTML بكل ملف باستخدام السمة "data" لوسم <object>.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")->get_Success());
}
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
