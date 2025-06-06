---
title: HtmlSaveOptions.OfficeMathOutputMode
linktitle: OfficeMathOutputMode
articleTitle: OfficeMathOutputMode
second_title: Aspose.Words per .NET
description: Scopri OfficeMathOutputMode di HtmlSaveOptions per esportazioni ottimali in HTML, MHTML o EPUB. Personalizza facilmente l'output degli oggetti OfficeMath!
type: docs
weight: 400
url: /it/net/aspose.words.saving/htmlsaveoptions/officemathoutputmode/
---
## HtmlSaveOptions.OfficeMathOutputMode property

Controlla come gli oggetti OfficeMath vengono esportati in HTML, MHTML o EPUB. Il valore predefinito èImage .

```csharp
public HtmlOfficeMathOutputMode OfficeMathOutputMode { get; set; }
```

## Esempi

Mostra come specificare come esportare oggetti Microsoft OfficeMath in HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare come l'operazione di salvataggio gestisce gli oggetti OfficeMath.
// Impostazione della proprietà "OfficeMathOutputMode" su "HtmlOfficeMathOutputMode.Image"
// trasformerà ogni oggetto OfficeMath in un'immagine.
// Impostazione della proprietà "OfficeMathOutputMode" su "HtmlOfficeMathOutputMode.MathML"
// convertirà ogni oggetto OfficeMath in MathML.
// Impostazione della proprietà "OfficeMathOutputMode" su "HtmlOfficeMathOutputMode.Text"
// rappresenterà ogni formula di OfficeMath utilizzando semplice testo HTML.
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

### Guarda anche

* enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
