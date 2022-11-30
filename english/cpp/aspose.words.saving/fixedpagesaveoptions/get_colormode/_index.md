---
title: get_ColorMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining how colors are rendered.
type: docs
weight: 14
url: /cpp/aspose.words.saving/fixedpagesaveoptions/get_colormode/
---
## FixedPageSaveOptions::get_ColorMode method


Gets or sets a value determining how colors are rendered.

```cpp
Aspose::Words::Saving::ColorMode Aspose::Words::Saving::FixedPageSaveOptions::get_ColorMode() const
```


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

* Enum [ColorMode](../../colormode/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
