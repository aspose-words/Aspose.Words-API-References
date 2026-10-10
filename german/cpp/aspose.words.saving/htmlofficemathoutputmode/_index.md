---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode Enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode Enum. Gibt an, wie Aspose.Words OfficeMath nach HTML, MHTML und EPUB in C++ exportiert."
type: docs
weight: 61000
url: /de/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


Gibt an, wie Aspose.Words OfficeMath nach HTML, MHTML und EPUB exportiert.

```cpp
enum class HtmlOfficeMathOutputMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Image | 0 | OfficeMath wird zu HTML als Bild konvertiert, das durch das <img>-Tag angegeben ist. |
| MathML | 1 | OfficeMath wird zu HTML unter Verwendung von MathML konvertiert. |
| Text | 2 | OfficeMath wird zu HTML als Folge von Runs konvertiert, die durch <span>-Tags angegeben sind. |


## Beispiele



Zeigt, wie man angibt, wie Microsoft OfficeMath-Objekte nach HTML exportiert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// Wenn wir das Dokument als HTML speichern, können wir ein SaveOptions‑Objekt übergeben
// um zu bestimmen, wie der Speicherungsprozess OfficeMath-Objekte behandelt.
// Festlegen der Eigenschaft "OfficeMathOutputMode" auf "HtmlOfficeMathOutputMode.Image"
// rendert jedes OfficeMath-Objekt in ein Bild.
// Festlegen der Eigenschaft "OfficeMathOutputMode" auf "HtmlOfficeMathOutputMode.MathML"
// konvertiert jedes OfficeMath-Objekt in MathML.
// Festlegen der Eigenschaft "OfficeMathOutputMode" auf "HtmlOfficeMathOutputMode.Text"
// stellt jede OfficeMath-Formel als reinen HTML-Text dar.
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
