---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.Saving.HtmlOfficeMathOutputMode den OfficeMath-Export nach HTML, MHTML und EPUB für eine nahtlose Dokumentkonvertierung verbessert.
type: docs
weight: 5850
url: /de/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Gibt an, wie Aspose.Words OfficeMath in HTML, MHTML und EPUB exportiert.

```csharp
public enum HtmlOfficeMathOutputMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Image | `0` | OfficeMath wird als durch den Tag &lt;img&gt; angegebenes Bild in HTML konvertiert. |
| MathML | `1` | OfficeMath wird mit MathML in HTML konvertiert. |
| Text | `2` | OfficeMath wird als durch &lt;span&gt;-Tags angegebene Abfolge von Läufen in HTML konvertiert. |

## Beispiele

Zeigt, wie Sie angeben, wie Microsoft OfficeMath-Objekte in HTML exportiert werden.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben
// um zu bestimmen, wie der Speichervorgang mit OfficeMath-Objekten umgeht.
// Festlegen der Eigenschaft „OfficeMathOutputMode“ auf „HtmlOfficeMathOutputMode.Image“
// rendert jedes OfficeMath-Objekt in ein Bild.
// Festlegen der Eigenschaft „OfficeMathOutputMode“ auf „HtmlOfficeMathOutputMode.MathML“
// konvertiert jedes OfficeMath-Objekt in MathML.
// Festlegen der Eigenschaft „OfficeMathOutputMode“ auf „HtmlOfficeMathOutputMode.Text“
// stellt jede OfficeMath-Formel mit einfachem HTML-Text dar.
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

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
