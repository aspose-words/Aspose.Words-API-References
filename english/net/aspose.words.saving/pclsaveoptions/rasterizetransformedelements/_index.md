---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
second_title: Aspose.Words for .NET API Reference
description: PclSaveOptions RasterizeTransformedElements property. Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is true in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Gets or sets a value determining whether or not complex transformed elements should be rasterized before saving to PCL document. Default is `true`.

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Remarks

PCL doesn't support some kind of transformations that are used by Aspose Words. E.g. rotated, skewed images and texture brushes. To properly render such elements rasterization process is used, i.e. saving to image and clipping. This process can take additional time and memory. If flag is set to `false`, some content in output may be different as compared with the source document.

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

* class [PclSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pclsaveoptions/)
* assembly [Aspose.Words](../../../)
