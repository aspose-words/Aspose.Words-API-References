---
title: PdfImageCompression enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the type of compression applied to images in the PDF file."
type: docs
weight: 640
url: /python-net/aspose.words.saving/pdfimagecompression/
---

## PdfImageCompression enumeration

Specifies the type of compression applied to images in the PDF file.


### Members

| Name | Description |
| --- | --- |
| AUTO | Automatically selects the most appropriate compression for each image. |
| JPEG | Jpeg compression. Does not support transparency. |

### Examples

Shows how to specify a compression type for all images in a document that we are converting to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Jpeg image:")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.insert_paragraph()
builder.writeln("Png image:")
builder.insert_image(IMAGE_DIR + "Transparent background logo.png")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()

# Set the "image_compression" property to "PdfImageCompression.AUTO" to use the
# "image_compression" property to control the quality of the Jpeg images that end up in the output PDF.
# Set the "image_compression" property to "PdfImageCompression.JPEG" to use the
# "image_compression" property to control the quality of all images that end up in the output PDF.
pdf_save_options.image_compression = pdf_image_compression

# Set the "jpeg_quality" property to "10" to strengthen compression at the cost of image quality.
pdf_save_options.jpeg_quality = 10

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.image_compression.pdf", pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

