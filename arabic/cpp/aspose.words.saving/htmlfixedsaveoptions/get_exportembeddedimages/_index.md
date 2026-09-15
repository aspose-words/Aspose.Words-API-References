---
title: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages"
linktitle: "get_ExportEmbeddedImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages. تحدد ما إذا كان يجب تضمين الصور في مستند Html بصيغة Base64. لاحظ أن ضبط هذه العلامة يمكن أن يزيد بشكل كبير من حجم ملف Html الناتج في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


يحدد ما إذا كان يجب تضمين الصور في مستند Html بتنسيق Base64. ملاحظة: ضبط هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف Html الناتج.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## أمثلة



يوضح كيفية تحديد مكان تخزين الصور عند تصدير مستند إلى Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// عند تصديرنا مستندًا يحتوي على صور مدمجة إلى .html،
// يمكن لـ Aspose.Words وضع الصور في موقعين محتملين.
// ضبط العلامة "ExportEmbeddedImages" إلى "true" سيخزن البيانات الخام
// لكل الصور داخل مستند HTML الناتج، في السمة "src" لعلامات <image>.
// ضبط هذه العلامة إلى "false" سيُنشئ ملف صورة في نظام الملفات المحلي لكل صورة،
// ويخزن جميع هذه الملفات في مجلد منفصل.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
