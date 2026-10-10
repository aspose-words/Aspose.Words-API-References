---
title: "التعداد Aspose::Words::Saving::HtmlMetafileFormat"
linktitle: "HtmlMetafileFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "التعداد Aspose::Words::Saving::HtmlMetafileFormat. يشير إلى الصيغة التي تُحفظ بها ملفات الميتا في مستندات HTML في C++."
type: docs
weight: 60000
url: /ar/cpp/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enum


يشير إلى التنسيق الذي تُحفظ به ملفات الميتا إلى مستندات HTML.

```cpp
enum class HtmlMetafileFormat
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Png | 0 | يتم تحويل ملفات الميتا إلى صور PNG نقطية. |
| Svg | 1 | يتم تحويل ملفات الميتا إلى صور SVG متجهة. |
| EmfOrWmf | 2 | يتم حفظ ملفات الميتا كما هي، دون تحويل. |


## أمثلة



يظهر كيفية تحويل كائنات SVG إلى صيغة مختلفة عند حفظ مستندات HTML.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// استخدم 'ConvertSvgToEmf' لإرجاع السلوك القديم
// حيث تم تحويل جميع صور SVG المحملة من مستند HTML إلى EMF.
// الآن تُحمَّل صور SVG دون تحويل
// إذا كان إصدار MS Word المحدد في خيارات التحميل يدعم صور SVG أصلاً.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// يحتوي هذا المستند على عنصر <svg> على شكل نص.
// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// لتحديد كيفية تعامل عملية الحفظ مع هذا الكائن.
// ضبط الخاصية "MetafileFormat" إلى "HtmlMetafileFormat.Png" لتحويله إلى صورة PNG.
// ضبط الخاصية "MetafileFormat" إلى "HtmlMetafileFormat.Svg" للحفاظ عليه ككائن SVG.
// ضبط الخاصية "MetafileFormat" إلى "HtmlMetafileFormat.EmfOrWmf" لتحويله إلى ملف ميتا.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
