---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words for .NET
description: Control the quality of your exported raster images with the SvgSaveOptions MaxImageResolution. Set pixel density for optimal results. Default: 0.
type: docs
weight: 50
url: /net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Gets or sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero.

```csharp
public int MaxImageResolution { get; set; }
```

## Remarks

If the value of this property is non-zero, it limits resolution of exported raster images. That is, higher-resolution images are resampled down to the limit and lower-resolution images are exported as is.

If the value of this property is zero, all raster images are exported without resampling.

## Examples

Shows how to set limit for image resolution.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### See Also

* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
