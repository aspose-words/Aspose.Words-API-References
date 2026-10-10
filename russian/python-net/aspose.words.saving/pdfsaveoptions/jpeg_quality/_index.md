---
title: PdfSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the JPEG images inside PDF document."
type: docs
weight: 240
url: /ru/python-net/aspose.words.saving/pdfsaveoptions/jpeg_quality/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# Установите свойство "ImageCompression" в значение "PdfImageCompression.Auto", чтобы использовать
# свойство "ImageCompression" для контроля качества JPEG‑изображений, попадающих в выходной PDF.
# Установите свойство "ImageCompression" в значение "PdfImageCompression.Jpeg", чтобы использовать
# свойство "ImageCompression" для контроля качества всех изображений, попадающих в выходной PDF.
pdf_save_options.image_compression = pdf_image_compression
# Установите свойство "JpegQuality" в значение "10", чтобы усилить сжатие за счёт качества изображения.
pdf_save_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageCompression.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

