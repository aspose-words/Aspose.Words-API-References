---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum. يحدد كيف يقوم Aspose.Words بتصدير OfficeMath إلى HTML وMHTML وEPUB في C++."
type: docs
weight: 61000
url: /ar/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى HTML و MHTML و EPUB.

```cpp
enum class HtmlOfficeMathOutputMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Image | 0 | يتم تحويل OfficeMath إلى HTML كصورة محددة بواسطة علامة <img>. |
| MathML | 1 | يتم تحويل OfficeMath إلى HTML باستخدام MathML. |
| Text | 2 | يتم تحويل OfficeMath إلى HTML كسلسلة من المقاطع المحددة بواسطة علامات <span>. |


## أمثلة



يوضح كيفية تحديد طريقة تصدير كائنات Microsoft OfficeMath إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// لتحديد كيفية تعامل عملية الحفظ مع كائنات OfficeMath.
// تعيين الخاصية "OfficeMathOutputMode" إلى "HtmlOfficeMathOutputMode.Image"
// سيتم عرض كل كائن OfficeMath كصورة.
// تعيين الخاصية "OfficeMathOutputMode" إلى "HtmlOfficeMathOutputMode.MathML"
// سيتم تحويل كل كائن OfficeMath إلى MathML.
// تعيين الخاصية "OfficeMathOutputMode" إلى "HtmlOfficeMathOutputMode.Text"
// سيتم تمثيل كل صيغة OfficeMath باستخدام نص HTML عادي.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_OfficeMathOutputMode(htmlOfficeMathOutputMode);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html", options);
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Image:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt\">") + u"<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " + u"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::MathML:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">") + u"<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" + u"<mi>i</mi>" + u"<mo>[+]</mo>" + u"<mi>b</mi>" + u"<mo>-</mo>" + u"<mi>c</mi>" + u"<mo>≥</mo>" + u".*" + u"</math>" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Text:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\\\"margin-top:0pt; margin-bottom:10pt; text-align:center\\\">") + u"<span style=\\\"font-family:'Cambria Math'\\\">i[+]b-c≥iM[+]bM-cM </span>" + u"</p>")->get_Success());
        break;

}
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
