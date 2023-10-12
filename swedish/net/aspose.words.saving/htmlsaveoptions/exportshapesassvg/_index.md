---
title: HtmlSaveOptions.ExportShapesAsSvg
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Styr omShapenoder konverteras till SVGbilder när save till HTML MHTML EPUB eller AZW3. Standardvärdet ärfalsk .
type: docs
weight: 250
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Styr om[`Shape`](../../../aspose.words.drawing/shape/)noder konverteras till SVG-bilder när save till HTML, MHTML, EPUB eller AZW3. Standardvärdet är`falsk` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

### Anmärkningar

Om det här alternativet är inställt på`Sann` ,[`Shape`](../../../aspose.words.drawing/shape/) noder exporteras som &lt;svg&gt;-element. Annars renderas de till bitmappar och exporteras som &lt;img&gt;-element.

### Exempel

Visar hur man exporterar form som skalbar vektorgrafik.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma hur sparoperationen kommer att exportera textruteformer.
// Om vi ställer in "ExportTextBoxAsSvg"-flaggan till "true",
// spara-operationen kommer att konvertera former med text till SVG-objekt.
// Om vi ställer in "ExportTextBoxAsSvg"-flaggan till "false",
// Spara operationen kommer att konvertera former med text till bilder.
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

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


