---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum. Spécifie comment Aspose.Words exporte OfficeMath vers HTML, MHTML et EPUB en C++."
type: docs
weight: 61000
url: /fr/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


Spécifie comment Aspose.Words exporte OfficeMath vers HTML, MHTML et EPUB.

```cpp
enum class HtmlOfficeMathOutputMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Image | 0 | OfficeMath est converti en HTML sous forme d'image spécifiée par la balise <img>. |
| MathML | 1 | OfficeMath est converti en HTML en utilisant MathML. |
| Texte | 2 | OfficeMath est converti en HTML sous forme de séquence de runs spécifiée par les balises <span>. |


## Exemples



Montre comment spécifier l'exportation des objets Microsoft OfficeMath vers HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// Lorsque nous enregistrons le document au format HTML, nous pouvons transmettre un objet SaveOptions
// pour déterminer comment l'opération d'enregistrement gère les objets OfficeMath.
// Définir la propriété "OfficeMathOutputMode" sur "HtmlOfficeMathOutputMode.Image"
// rendra chaque objet OfficeMath sous forme d'image.
// Définir la propriété "OfficeMathOutputMode" sur "HtmlOfficeMathOutputMode.MathML"
// convertira chaque objet OfficeMath en MathML.
// Définir la propriété "OfficeMathOutputMode" sur "HtmlOfficeMathOutputMode.Text"
// représentera chaque formule OfficeMath en texte HTML simple.
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

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
