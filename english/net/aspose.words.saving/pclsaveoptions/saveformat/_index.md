---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
second_title: Aspose.Words for .NET API Reference
description: PclSaveOptions SaveFormat property. Specifies the format in which the document will be saved if this save options object is used. Can only be Pcl in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/pclsaveoptions/saveformat/
---
## SaveFormat property

Specifies the format in which the document will be saved if this save options object is used. Can only be Pcl.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Examples

Shows how to rasterize complex elements while saving a document to PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pclsaveoptions/)
* assembly [Aspose.Words](../../../)
