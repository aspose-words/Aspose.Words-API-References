---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts طريقة"
linktitle: "get_ExportEmbeddedFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts طريقة. يحدد ما إذا كان يجب تضمين الخطوط في مستند Html بصيغة Base64. لاحظ أن ضبط هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف Html الناتج في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


يحدد ما إذا كان يجب تضمين الخطوط في مستند Html بتنسيق Base64. ملاحظة: ضبط هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف Html الناتج.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## أمثلة



يوضح كيفية تحديد مكان تخزين الخطوط المضمنة عند تصدير مستند إلى Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// عند تصدير مستند يحتوي على خطوط مضمّنة إلى .html،
// يمكن لـ Aspose.Words وضع الخطوط في موقعين محتملين.
// ضبط علم "ExportEmbeddedFonts" إلى "true" سيخزن البيانات الخام للخطوط المضمنة داخل ورقة أنماط CSS،
// في خاصية "url" لقاعدة "@font-face". قد يؤدي ذلك إلى إنشاء ملف ورقة أنماط CSS ضخم
// ويقلل عدد الملفات الخارجية التي سيُنشئها هذا التحويل إلى HTML.
// تعيين هذه العلامة إلى "false" سيؤدي إلى إنشاء ملف لكل خط.
// ستربط ورقة أنماط CSS كل ملف خط باستخدام خاصية "url" لقاعدة "@font-face".
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
