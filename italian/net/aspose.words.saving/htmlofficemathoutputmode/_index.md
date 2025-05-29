---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.Saving.HtmlOfficeMathOutputMode migliora l'esportazione di OfficeMath in HTML, MHTML ed EPUB per una conversione fluida dei documenti.
type: docs
weight: 5850
url: /it/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Specifica come Aspose.Words esporta OfficeMath in HTML, MHTML ed EPUB.

```csharp
public enum HtmlOfficeMathOutputMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Image | `0` | OfficeMath viene convertito in HTML come immagine specificata dal tag &lt;img&gt;. |
| MathML | `1` | OfficeMath viene convertito in HTML utilizzando MathML. |
| Text | `2` | OfficeMath viene convertito in HTML come sequenza di esecuzioni specificate dai tag &lt;span&gt;. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
