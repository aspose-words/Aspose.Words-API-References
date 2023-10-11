---
title: HtmlSaveOptions.ExportShapesAsSvg
second_title: Référence de l'API Aspose.Words pour .NET
description: HtmlSaveOptions propriété. Contrôle siShapeles nœuds sont convertis en images SVG lors de la sauvegarde de au format HTML MHTML EPUB ou AZW3. La valeur par défaut estFAUX .
type: docs
weight: 250
url: /fr/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Contrôle si[`Shape`](../../../aspose.words.drawing/shape/)les nœuds sont convertis en images SVG lors de la sauvegarde de au format HTML, MHTML, EPUB ou AZW3. La valeur par défaut est`FAUX` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

### Remarques

Si cette option est définie sur`vrai` ,[`Shape`](../../../aspose.words.drawing/shape/) les nœuds sont exportés sous forme d'éléments &lt;svg&gt;. Sinon, ils sont rendus en bitmaps et exportés sous forme d'éléments &lt;img&gt;.

### Exemples

Montre comment exporter une forme sous forme de graphiques vectoriels évolutifs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions
// pour déterminer comment l'opération de sauvegarde exportera les formes de zone de texte.
// Si on met le flag "ExportTextBoxAsSvg" à "true",
// l'opération de sauvegarde convertira les formes avec du texte en objets SVG.
// Si on met le flag "ExportTextBoxAsSvg" à "false",
// l'opération de sauvegarde convertira les formes avec du texte en images.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height= \"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../htmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


