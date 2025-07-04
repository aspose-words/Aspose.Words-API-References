---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words for .NET
description: Discover how the ExportEmbeddedImages property in HtmlFixedSaveOptions enhances your HTML documents by embedding images in Base64 format, optimizing visual quality while managing file size.
type: docs
weight: 60
url: /net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Examples

Shows how to determine where to store images when exporting a document to Html.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// When we export a document with embedded images to .html,
// Aspose.Words can place the images in two possible locations.
// Setting the "ExportEmbeddedImages" flag to "true" will store the raw data
// for all images within the output HTML document, in the "src" attribute of <image> tags.
// Setting this flag to "false" will create an image file in the local file system for every image,
// and store all these files in a separate folder.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.That(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"), Is.False);
    Assert.That(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success, Is.True);
}
else
{
    Assert.That(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"), Is.True);
    Assert.That(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success, Is.True);
}
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
