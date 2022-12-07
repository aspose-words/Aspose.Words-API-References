---
title: get_ImageColorSpaceExportMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how the color space will be selected for the images in PDF document.
type: docs
weight: 248
url: /cpp/aspose.words.saving/pdfsaveoptions/get_imagecolorspaceexportmode/
---
## PdfSaveOptions::get_ImageColorSpaceExportMode method


Specifies how the color space will be selected for the images in PDF document.

```cpp
Aspose::Words::Saving::PdfImageColorSpaceExportMode Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode() const
```

## Remarks


The default value is [Auto](../../pdfimagecolorspaceexportmode/).

If [SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is specified, [ImageCompression](../get_imagecompression/) option is ignored and Flate compression is used for all images in the document.

[SimpleCmyk](../../pdfimagecolorspaceexportmode/) value is not supported when saving to PDF/A. [Auto](../../pdfimagecolorspaceexportmode/) value will be used instead.

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

* Enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
