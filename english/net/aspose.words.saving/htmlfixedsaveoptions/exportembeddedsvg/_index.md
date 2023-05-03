---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
second_title: Aspose.Words for .NET API Reference
description: HtmlFixedSaveOptions ExportEmbeddedSvg property. Specifies whether SVG resources should be embedded into Html document. Default value is true in C#.
type: docs
weight: 70
url: /net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## ExportEmbeddedSvg property

Specifies whether SVG resources should be embedded into Html document. Default value is `true`.

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Examples

Shows how to determine where to store SVG objects when exporting a document to Html.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// When we export a document with SVG objects to .html,
// Aspose.Words can place these objects in two possible locations.
// Setting the "ExportEmbeddedSvg" flag to "true" will embed all SVG object raw data
// within the output HTML, inside <image> tags.
// Setting this flag to "false" will create a file in the local file system for each SVG object.
// The HTML will link to each file using the "data" attribute of an <object> tag.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assembly [Aspose.Words](../../../)
