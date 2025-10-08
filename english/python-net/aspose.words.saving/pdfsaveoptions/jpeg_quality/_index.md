---
title: PdfSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the JPEG images inside PDF document."
type: docs
weight: 230
url: /python-net/aspose.words.saving/pdfsaveoptions/jpeg_quality/
---

## PdfSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the JPEG images inside PDF document.


```python
@property
def jpeg_quality(self) -> int:
    ...

@jpeg_quality.setter
def jpeg_quality(self, value: int):
    ...

```

### Remarks

The default value is 100.

This property is used in conjunction with the [PdfSaveOptions.image_compression](../image_compression/) option.

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in PDF format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.
If quality is 100 and source image is JPEG, it means no compression - original bytes will be saved.




### Examples

Shows how to specify a compression type for all images in a document that we are converting to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jpeg image:')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_paragraph()
builder.writeln('Png image:')
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Set the "ImageCompression" property to "PdfImageCompression.Auto" to use the
# "ImageCompression" property to control the quality of the Jpeg images that end up in the output PDF.
# Set the "ImageCompression" property to "PdfImageCompression.Jpeg" to use the
# "ImageCompression" property to control the quality of all images that end up in the output PDF.
pdf_save_options.image_compression = pdf_image_compression
# Set the "JpegQuality" property to "10" to strengthen compression at the cost of image quality.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

