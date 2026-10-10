---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode metod"
linktitle: "get_OfficeMathOutputMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode metod. Styr hur OfficeMath-objekt exporteras till HTML, MHTML eller EPUB. Standardvärdet är Image i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_officemathoutputmode/
---
## HtmlSaveOptions::get_OfficeMathOutputMode method


Styr hur OfficeMath-objekt exporteras till HTML, MHTML eller EPUB. Standardvärdet är [Image](../../htmlofficemathoutputmode/).

```cpp
Aspose::Words::Saving::HtmlOfficeMathOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode() const
```


## Exempel



Visar hur man specificerar export av Microsoft OfficeMath-objekt till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma hur sparningsoperationen hanterar OfficeMath-objekt.
// Ställer in egenskapen "OfficeMathOutputMode" till "HtmlOfficeMathOutputMode.Image"
// kommer att rendera varje OfficeMath-objekt till en bild.
// Ställer in egenskapen "OfficeMathOutputMode" till "HtmlOfficeMathOutputMode.MathML"
// kommer att konvertera varje OfficeMath-objekt till MathML.
// Ställer in egenskapen "OfficeMathOutputMode" till "HtmlOfficeMathOutputMode.Text"
// kommer att representera varje OfficeMath-formel med vanlig HTML-text.
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

## Se även

* Enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
