---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words for .NET
description: Discover how the HtmlSaveOptions ExportPageMargins property enhances your HTML, MHTML, and EPUB exports by controlling page margins for a polished presentation.
type: docs
weight: 210
url: /net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is `false`.

```csharp
public bool ExportPageMargins { get; set; }
```

## Remarks

Aspose.Words does not show area of page margins by default. If any elements are completely or partially clipped by the document edge the displayed area can be extended with this option.

## Examples

Shows how to show out-of-bounds objects in output HTML documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a builder to insert a shape with no wrapping.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Negative shape position values may place the shape outside of page boundaries.
// If we export this to HTML, the shape will appear truncated.
shape.Left = -150;

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to adjust the page to display out-of-bounds objects fully.
// If we set the "ExportPageMargins" flag to "true", the shape will be fully visible in the output HTML.
// If we set the "ExportPageMargins" flag to "false",
// our document will display the shape truncated as we would see it in Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.That(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"), Is.True);
    Assert.That(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"), Is.True);
}
else
{
    Assert.That(outDocContents.Contains("style type=\"text/css\">"), Is.False);
    Assert.That(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"), Is.True);
}
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
