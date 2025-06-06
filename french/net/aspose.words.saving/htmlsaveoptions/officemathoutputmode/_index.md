---
title: HtmlSaveOptions.OfficeMathOutputMode
linktitle: OfficeMathOutputMode
articleTitle: OfficeMathOutputMode
second_title: Aspose.Words pour .NET
description: Découvrez le mode OfficeMathOutputMode de HtmlSaveOptions pour des exportations HTML, MHTML ou EPUB optimales. Personnalisez facilement la sortie des objets OfficeMath !
type: docs
weight: 400
url: /fr/net/aspose.words.saving/htmlsaveoptions/officemathoutputmode/
---
## HtmlSaveOptions.OfficeMathOutputMode property

Contrôle la manière dont les objets OfficeMath sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut estImage .

```csharp
public HtmlOfficeMathOutputMode OfficeMathOutputMode { get; set; }
```

## Exemples

Montre comment spécifier comment exporter des objets Microsoft OfficeMath vers HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions
// pour déterminer comment l'opération de sauvegarde gère les objets OfficeMath.
// Définition de la propriété « OfficeMathOutputMode » sur « HtmlOfficeMathOutputMode.Image »
// rendra chaque objet OfficeMath dans une image.
// Définition de la propriété « OfficeMathOutputMode » sur « HtmlOfficeMathOutputMode.MathML »
// convertira chaque objet OfficeMath en MathML.
// Définition de la propriété « OfficeMathOutputMode » sur « HtmlOfficeMathOutputMode.Text »
// représentera chaque formule OfficeMath à l'aide de texte HTML brut.
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

### Voir également

* enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
