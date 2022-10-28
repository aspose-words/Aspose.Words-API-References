---
title: get_ImageCompression
second_title: Aspose.Words for C++ API Reference
description: Specifies compression type to be used for all images in the document.
type: docs
weight: 235
url: /cpp/aspose.words.saving/pdfsaveoptions/get_imagecompression/
---
## PdfSaveOptions.get_ImageCompression method


Specifies compression type to be used for all images in the document.

```cpp
Aspose::Words::Saving::PdfImageCompression Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression() const
```


Default is **Auto**.

Using **Jpeg** lets you control the quality of images in the output document through the [JpegQuality](../get_jpegquality/) property.

Using **Jpeg** provides the fastest conversion speed when compared to the performance of other compression types, but in this case, there is lossy JPEG compression.

Using **Auto** lets to control the quality of Jpeg in the output document through the [JpegQuality](../get_jpegquality/) property, but for other formats, raw pixel data is extracted and saved with Flate compression. This case is slower than Jpeg conversion but lossless.

## Examples




Shows how to specify a compression type for all images in a document that we are converting to PDF. 
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

// Set the "ImageCompression" property to "PdfImageCompression.Auto" to use the
// "ImageCompression" property to control the quality of the Jpeg images that end up in the output PDF.
// Set the "ImageCompression" property to "PdfImageCompression.Jpeg" to use the
// "ImageCompression" property to control the quality of all images that end up in the output PDF.
pdfSaveOptions->set_ImageCompression(pdfImageCompression);

// Set the "JpegQuality" property to "10" to strengthen compression at the cost of image quality.
pdfSaveOptions->set_JpegQuality(10);

doc->Save(ArtifactsDir + u"PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

