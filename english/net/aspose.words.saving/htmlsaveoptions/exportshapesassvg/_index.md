---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions property. Controls whether Shape nodes are converted to SVG images when saving to HTML MHTML EPUB or AZW3. Default value is false in C#.
type: docs
weight: 260
url: /net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Controls whether [`Shape`](../../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is `false`.

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## Remarks

If this option is set to `true`, [`Shape`](../../../aspose.words.drawing/shape/) nodes are exported as &lt;svg&gt; elements. Otherwise, they are rendered to bitmaps and are exported as &lt;img&gt; elements.

## Examples

Shows how to export shape as scalable vector graphics.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation will export text box shapes.
// If we set the "ExportTextBoxAsSvg" flag to "true",
// the save operation will convert shapes with text into SVG objects.
// If we set the "ExportTextBoxAsSvg" flag to "false",
// the save operation will convert shapes with text into images.
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

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)
