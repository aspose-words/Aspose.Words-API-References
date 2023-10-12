---
title: HtmlSaveOptions.OfficeMathOutputMode
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Controla cómo se exportan los objetos de OfficeMath a HTML MHTML o EPUB. El valor predeterminado esImage .
type: docs
weight: 400
url: /es/net/aspose.words.saving/htmlsaveoptions/officemathoutputmode/
---
## HtmlSaveOptions.OfficeMathOutputMode property

Controla cómo se exportan los objetos de OfficeMath a HTML, MHTML o EPUB. El valor predeterminado esImage .

```csharp
public HtmlOfficeMathOutputMode OfficeMathOutputMode { get; set; }
```

### Ejemplos

Muestra cómo especificar cómo exportar objetos de Microsoft OfficeMath a HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardar maneja los objetos de OfficeMath.
// Estableciendo la propiedad "OfficeMathOutputMode" en "HtmlOfficeMathOutputMode.Image"
// representará cada objeto de OfficeMath en una imagen.
// Estableciendo la propiedad "OfficeMathOutputMode" en "HtmlOfficeMathOutputMode.MathML"
// convertirá cada objeto de OfficeMath en MathML.
// Estableciendo la propiedad "OfficeMathOutputMode" en "HtmlOfficeMathOutputMode.Text"
// representará cada fórmula de OfficeMath utilizando texto HTML sin formato.
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.True(Regex.Match(outDocContents, 
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"159\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
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

* enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


