---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum. Specifica come Aspose.Words esporta OfficeMath in HTML, MHTML ed EPUB in C++."
type: docs
weight: 61000
url: /it/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


Specifica come Aspose.Words esporta OfficeMath in HTML, MHTML ed EPUB.

```cpp
enum class HtmlOfficeMathOutputMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Immagine | 0 | OfficeMath viene convertito in HTML come immagine specificata dal tag <img>. |
| MathML | 1 | OfficeMath viene convertito in HTML utilizzando MathML. |
| Testo | 2 | OfficeMath viene convertito in HTML come sequenza di run specificata dai tag <span>. |


## Esempi



Mostra come specificare l'esportazione degli oggetti Microsoft OfficeMath in HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare come l'operazione di salvataggio gestisce gli oggetti OfficeMath.
// Impostazione della proprietà "OfficeMathOutputMode" su "HtmlOfficeMathOutputMode.Image"
// renderizzerà ogni oggetto OfficeMath in un'immagine.
// Impostazione della proprietà "OfficeMathOutputMode" su "HtmlOfficeMathOutputMode.MathML"
// converterà ogni oggetto OfficeMath in MathML.
// Impostazione della proprietà "OfficeMathOutputMode" su "HtmlOfficeMathOutputMode.Text"
// rappresenterà ogni formula OfficeMath usando testo HTML semplice.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
