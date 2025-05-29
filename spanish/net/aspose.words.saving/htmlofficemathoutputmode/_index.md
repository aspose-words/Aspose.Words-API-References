---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words para .NET
description: Descubra cómo Aspose.Words.Saving.HtmlOfficeMathOutputMode mejora la exportación de OfficeMath a HTML, MHTML y EPUB para una conversión de documentos perfecta.
type: docs
weight: 5850
url: /es/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Especifica cómo Aspose.Words exporta OfficeMath a HTML, MHTML y EPUB.

```csharp
public enum HtmlOfficeMathOutputMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Image | `0` | OfficeMath se convierte a HTML como imagen especificada por la etiqueta &lt;img&gt;. |
| MathML | `1` | OfficeMath se convierte a HTML usando MathML. |
| Text | `2` | OfficeMath se convierte a HTML como una secuencia de ejecuciones especificadas por las etiquetas &lt;span&gt;. |

## Ejemplos

Muestra cómo especificar cómo exportar objetos de Microsoft OfficeMath a HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardado maneja los objetos de OfficeMath.
// Estableciendo la propiedad "OfficeMathOutputMode" en "HtmlOfficeMathOutputMode.Image"
// convertirá cada objeto OfficeMath en una imagen.
// Estableciendo la propiedad "OfficeMathOutputMode" en "HtmlOfficeMathOutputMode.MathML"
// convertirá cada objeto OfficeMath en MathML.
// Estableciendo la propiedad "OfficeMathOutputMode" en "HtmlOfficeMathOutputMode.Text"
// representará cada fórmula de OfficeMath utilizando texto HTML simple.
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                "-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.MathML:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">" +
                "<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" +
                    "<mi>i</mi>" +
                    "<mo>[+]</mo>" +
                    "<mi>b</mi>" +
                    "<mo>-</mo>" +
                    "<mi>c</mi>" +
                    "<mo>≥</mo>" +
                    ".*" +
                "</math>" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.Text:
        Assert.True(Regex.Match(outDocContents,
            @"<p style=\""margin-top:0pt; margin-bottom:10pt; text-align:center\"">" +
                @"<span style=\""font-family:'Cambria Math'\"">i[+]b-c≥iM[+]bM-cM </span>" +
            "</p>").Success);
        break;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
