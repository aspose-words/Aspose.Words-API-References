---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum. Anger hur Aspose.Words exporterar OfficeMath till HTML, MHTML och EPUB i C++."
type: docs
weight: 61000
url: /sv/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


Anger hur Aspose.Words exporterar OfficeMath till HTML, MHTML och EPUB.

```cpp
enum class HtmlOfficeMathOutputMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Image | 0 | OfficeMath konverteras till HTML som en bild som anges av <img>-taggen. |
| MathML | 1 | OfficeMath konverteras till HTML med hjälp av MathML. |
| Text | 2 | OfficeMath konverteras till HTML som en sekvens av körningar som anges av <span>-taggar. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
