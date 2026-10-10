---
title: ImageSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the generated JPEG images."
type: docs
weight: 70
url: /es/python-net/aspose.words.saving/imagesaveoptions/jpeg_quality/
---

## ImageSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the generated JPEG images.


```python
@property
def jpeg_quality(self) -> int:
    ...

@jpeg_quality.setter
def jpeg_quality(self, value: int):
    ...

```

### Remarks

Has effect only when saving to JPEG.

Use this property to get or set the quality of generated images when saving in JPEG format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
# para modificar la forma en que ese método renderiza el documento en una imagen.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Establezca la propiedad "JpegQuality" en "10" para usar una compresión más fuerte al renderizar el documento.
# Esto reducirá el tamaño del archivo del documento, pero la imagen mostrará artefactos de compresión más notorios.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Establezca la propiedad "JpegQuality" en "100" para usar una compresión más débil al renderizar el documento.
# Esto mejorará la calidad de la imagen a costa de un aumento del tamaño del archivo.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

