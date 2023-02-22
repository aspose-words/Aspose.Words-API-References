---
title: Enum HtmlOfficeMathOutputMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.HtmlOfficeMathOutputMode énumération. Spécifie comment Aspose.Words exporte OfficeMath vers HTML MHTML et EPUB.
type: docs
weight: 4840
url: /fr/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Spécifie comment Aspose.Words exporte OfficeMath vers HTML, MHTML et EPUB.

```csharp
public enum HtmlOfficeMathOutputMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Image | `0` | OfficeMath est converti en HTML en tant qu'image spécifiée par la balise &lt;img&gt;. |
| MathML | `1` | OfficeMath est converti en HTML à l'aide de MathML. |
| Text | `2` | OfficeMath est converti en HTML en tant que séquence d'exécutions spécifiée par les balises &lt;span&gt;. |

### Exemples

Montre comment spécifier comment exporter des objets Microsoft OfficeMath au format HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions
// pour déterminer comment l'opération d'enregistrement gère les objets OfficeMath.
// Définition de la propriété "OfficeMathOutputMode" sur "HtmlOfficeMathOutputMode.Image"
// rendra chaque objet OfficeMath dans une image.
// Définition de la propriété "OfficeMathOutputMode" sur "HtmlOfficeMathOutputMode.MathML"
// convertira chaque objet OfficeMath en MathML.
// Définition de la propriété "OfficeMathOutputMode" sur "HtmlOfficeMathOutputMode.Text"
// représentera chaque formule OfficeMath en utilisant du texte HTML brut.
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

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


