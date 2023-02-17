---
title: PdfImageColorSpaceExportMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how the color space will be selected for the images in PDF document.
type: docs
weight: 989
url: /cpp/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enum


Specifies how the color space will be selected for the images in PDF document.

```cpp
enum class PdfImageColorSpaceExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 0 | Aspose.Words automatically selects the most appropriate color space for each image. |
| SimpleCmyk | 1 | Aspose.Words coverts RGB images to CMYK color space using simple formula. |


## Examples



Shows how to set a different color space for images in a document as we export it to PDF. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Jpeg image:");
builder->InsertImage(ImageDir + u"Logo.jpg");
builder->InsertParagraph();
builder->Writeln(u"Png image:");
builder->InsertImage(ImageDir + u"Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto pdfSaveOptions = MakeObject<PdfSaveOptions>();

// Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
// automatically select the color space for images in the document that it converts to PDF.
// In most cases, the color space will be RGB.
// Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
// to use the CMYK color space for all images in the saved PDF.
// Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
pdfSaveOptions->set_ImageColorSpaceExportMode(pdfImageColorSpaceExportMode);

doc->Save(ArtifactsDir + u"PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
