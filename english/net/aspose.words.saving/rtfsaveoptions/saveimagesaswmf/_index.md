---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words for .NET
description: Discover how the RtfSaveOptions SaveImagesAsWmf property enhances your document by saving all images as WMF for superior quality and compatibility.
type: docs
weight: 50
url: /net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

When `true` all images will be saved as WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Remarks

This option might help to avoid WordPad warning messages.

## Examples

Shows how to convert all images in a document to the Windows Metafile format as we save the document as an RTF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.That(imageShape.ImageData.ImageType, Is.EqualTo(ImageType.Jpeg));

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.That(imageShape.ImageData.ImageType, Is.EqualTo(ImageType.Png));

// Create an "RtfSaveOptions" object to pass to the document's "Save" method to modify how we save it to an RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Set the "SaveImagesAsWmf" property to "true" to convert all images in the document to WMF as we save it to RTF.
// Doing so will help readers such as WordPad to read our document.
// Set the "SaveImagesAsWmf" property to "false" to preserve the original format of all images in the document
// as we save it to RTF. This will preserve the quality of the images at the cost of compatibility with older RTF readers.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.That(((Shape)shapes[0]).ImageData.ImageType, Is.EqualTo(ImageType.Wmf));
    Assert.That(((Shape)shapes[1]).ImageData.ImageType, Is.EqualTo(ImageType.Wmf));
}
else
{
    Assert.That(((Shape)shapes[0]).ImageData.ImageType, Is.EqualTo(ImageType.Jpeg));
    Assert.That(((Shape)shapes[1]).ImageData.ImageType, Is.EqualTo(ImageType.Png));
}
```

### See Also

* class [RtfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
