---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode método"
linktitle: "get_OfficeMathOutputMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode método. Controla cómo se exportan los objetos OfficeMath a HTML, MHTML o EPUB. El valor predeterminado es Image en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_officemathoutputmode/
---
## HtmlSaveOptions::get_OfficeMathOutputMode method


Controla cómo se exportan los objetos OfficeMath a HTML, MHTML o EPUB. El valor predeterminado es [Image](../../htmlofficemathoutputmode/).

```cpp
Aspose::Words::Saving::HtmlOfficeMathOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode() const
```


## Ejemplos



Muestra cómo especificar la exportación de objetos Microsoft OfficeMath a HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardado maneja los objetos OfficeMath.
// Estableciendo la propiedad "OfficeMathOutputMode" a "HtmlOfficeMathOutputMode.Image"
// renderizará cada objeto OfficeMath en una imagen.
// Estableciendo la propiedad "OfficeMathOutputMode" a "HtmlOfficeMathOutputMode.MathML"
// convertirá cada objeto OfficeMath a MathML.
// Estableciendo la propiedad "OfficeMathOutputMode" a "HtmlOfficeMathOutputMode.Text"
// representará cada fórmula OfficeMath usando texto HTML plano.
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

## Ver también

* Enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
