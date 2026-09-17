---
title: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode"
linktitle: "get_OfficeMathOutputMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode. Contrôle la façon dont les objets OfficeMath sont exportés en HTML, MHTML ou EPUB. La valeur par défaut est Image en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_officemathoutputmode/
---
## HtmlSaveOptions::get_OfficeMathOutputMode method


Contrôle la façon dont les objets OfficeMath sont exportés en HTML, MHTML ou EPUB. La valeur par défaut est [Image](../../htmlofficemathoutputmode/).

```cpp
Aspose::Words::Saving::HtmlOfficeMathOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode() const
```


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

* Enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
