---
title: ColorMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how colors are rendered.
type: docs
weight: 586
url: /cpp/aspose.words.saving/colormode/
---
## ColorMode enum


Specifies how colors are rendered.

```cpp
enum class ColorMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | 0 | [Rendering](../../aspose.words.rendering/) with unmodified colors. |
| Grayscale | 1 | [Rendering](../../aspose.words.rendering/) with colors in a range of gray shades from white to black. |


## Examples



Shows how to change image color with saving options property. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
// The size of the output document may be larger with this setting.
// Set the "ColorMode" property to "Normal" to render all images in color.
auto pdfSaveOptions = MakeObject<PdfSaveOptions>();
pdfSaveOptions->set_ColorMode(colorMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
