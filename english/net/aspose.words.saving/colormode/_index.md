---
title: ColorMode Enum
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.ColorMode enum for optimized color rendering. Enhance your document's visual appeal with precise color settings.
type: docs
weight: 5460
url: /net/aspose.words.saving/colormode/
---
## ColorMode enumeration

Specifies how colors are rendered.

```csharp
public enum ColorMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | `0` | Rendering with unmodified colors. |
| Grayscale | `1` | Rendering with colors in a range of gray shades from white to black. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
