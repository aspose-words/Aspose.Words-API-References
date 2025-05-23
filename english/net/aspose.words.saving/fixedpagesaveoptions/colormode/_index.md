---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words for .NET
description: Discover the FixedPageSaveOptions ColorMode property to customize color rendering for enhanced document quality and visual appeal. Optimize your output today!
type: docs
weight: 10
url: /net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Gets or sets a value determining how colors are rendered.

```csharp
public ColorMode ColorMode { get; set; }
```

## Remarks

The default value is Normal.

## Examples

Shows how to change image color with saving options property.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
// The size of the output document may be larger with this setting.
// Set the "ColorMode" property to "Normal" to render all images in color.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### See Also

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
