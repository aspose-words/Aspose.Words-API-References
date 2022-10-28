---
title: image_compression property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies compression type to be used for all images in the document."
type: docs
weight: 190
url: /python-net/aspose.words.saving/pdfsaveoptions/image_compression/
---

## PdfSaveOptions.image_compression property

Specifies compression type to be used for all images in the document.

Default is [PdfImageCompression.AUTO](../../pdfimagecompression/#AUTO).

Using [PdfImageCompression.JPEG](../../pdfimagecompression/#JPEG) lets you control the quality of images in the output document through the [PdfSaveOptions.jpeg_quality](../jpeg_quality/) property.

Using [PdfImageCompression.JPEG](../../pdfimagecompression/#JPEG) provides the fastest conversion speed when compared to the performance of other compression types,
but in this case, there is lossy JPEG compression.

Using [PdfImageCompression.AUTO](../../pdfimagecompression/#AUTO) lets to control the quality of Jpeg in the output document through the [PdfSaveOptions.jpeg_quality](../jpeg_quality/) property,
but for other formats, raw pixel data is extracted and saved with Flate compression.
This case is slower than Jpeg conversion but lossless.




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

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

