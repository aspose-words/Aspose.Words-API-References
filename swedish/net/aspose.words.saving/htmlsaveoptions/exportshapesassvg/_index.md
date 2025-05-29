---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
articleTitle: ExportShapesAsSvg
second_title: Aspose.Words för .NET
description: Upptäck hur du använder HtmlSaveOptions ExportShapesAsSvg för att konvertera Shape-noder till SVG-bilder när du sparar i HTML-, MHTML-, EPUB- eller AZW3-format.
type: docs
weight: 250
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Kontrollerar om[`Shape`](../../../aspose.words.drawing/shape/)noder konverteras till SVG-bilder när de sparas till HTML, MHTML, EPUB eller AZW3. Standardvärdet är`falsk` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## Anmärkningar

Om det här alternativet är inställt på`sann` ,[`Shape`](../../../aspose.words.drawing/shape/) noder exporteras som &lt;svg&gt;-element. Annars renderas de till bitmappar och exporteras som &lt;img&gt;-element.

## Exempel

Visar hur man exporterar former som skalbar vektorgrafik.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma hur textruteformer exporteras vid sparandet.
// Om vi ställer in flaggan "ExportTextBoxAsSvg" till "true",
// sparoperationen konverterar former med text till SVG-objekt.
// Om vi sätter flaggan "ExportTextBoxAsSvg" till "false",
// sparoperationen konverterar former med text till bilder.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
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
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
