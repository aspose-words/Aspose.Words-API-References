---
title: get_OfficeMathOutputMode
second_title: Aspose.Words for C++ API Reference
description: Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is Image.
type: docs
weight: 521
url: /cpp/aspose.words.saving/htmlsaveoptions/get_officemathoutputmode/
---
## HtmlSaveOptions::get_OfficeMathOutputMode method


Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [Image](../../htmlofficemathoutputmode/).

```cpp
Aspose::Words::Saving::HtmlOfficeMathOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode() const
```


## Examples



Shows how to specify how to export Microsoft OfficeMath objects to HTML. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation handles OfficeMath objects.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
// will render each OfficeMath object into an image.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
// will convert each OfficeMath object into MathML.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
// will represent each OfficeMath formula using plain HTML text.
auto options = MakeObject<HtmlSaveOptions>();
options->set_OfficeMathOutputMode(htmlOfficeMathOutputMode);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.OfficeMathOutputMode.html", options);
String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
case HtmlOfficeMathOutputMode::Image:
    ASSERT_TRUE(
        System::Text::RegularExpressions::Regex::Match(
            outDocContents,
            String(u"<p style=\"margin-top:0pt; margin-bottom:10pt\">") +
                u"<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"159\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                u"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>")
            ->get_Success());
    break;

case HtmlOfficeMathOutputMode::MathML:
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, String(u"<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">") +
                                        u"<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" + u"<mi>i</mi>" + u"<mo>[+]</mo>" + u"<mi>b</mi>" +
                                        u"<mo>-</mo>" + u"<mi>c</mi>" + u"<mo>≥</mo>" + u".*" + u"</math>" + u"</p>")
                    ->get_Success());
    break;

case HtmlOfficeMathOutputMode::Text:
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, String(u"<p style=\\\"margin-top:0pt; margin-bottom:10pt; text-align:center\\\">") +
                                        u"<span style=\\\"font-family:'Cambria Math'\\\">i[+]b-c≥iM[+]bM-cM </span>" + u"</p>")
                    ->get_Success());
    break;
}
```

## See Also

* Enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
