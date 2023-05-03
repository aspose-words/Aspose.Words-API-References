---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
second_title: Aspose.Words for .NET API Reference
description: PdfSaveOptions ImageColorSpaceExportMode property. Specifies how the color space will be selected for the images in PDF document in C#.
type: docs
weight: 190
url: /net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## ImageColorSpaceExportMode property

Specifies how the color space will be selected for the images in PDF document.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## Remarks

The default value is Auto.

If SimpleCmyk value is specified, [`ImageCompression`](../imagecompression/) option is ignored and Flate compression is used for all images in the document.

SimpleCmyk value is not supported when saving to PDF/A. Auto value will be used instead.

## Examples

Shows how to set a different color space for images in a document as we export it to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
// automatically select the color space for images in the document that it converts to PDF.
// In most cases, the color space will be RGB.
// Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
// to use the CMYK color space for all images in the saved PDF.
// Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### See Also

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
