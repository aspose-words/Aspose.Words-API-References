---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /ru/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
---

## ImageSaveOptions.tiff_compression property

Gets or sets the type of compression to apply when saving generated images to the TIFF format.


```python
@property
def tiff_compression(self) -> aspose.words.saving.TiffCompression:
    ...

@tiff_compression.setter
def tiff_compression(self, value: aspose.words.saving.TiffCompression):
    ...

```

### Remarks

Has effect only when saving to TIFF.

The default value is [TiffCompression.LZW](../../tiffcompression/#LZW).




### Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в изображение.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# Установите свойство "TiffCompression" в "TiffCompression.None", чтобы не применять сжатие при сохранении,
# что может привести к очень большому выходному файлу.
# Установите свойство "TiffCompression" в "TiffCompression.Rle", чтобы применить RLE‑сжатие
# Установите свойство "TiffCompression" в "TiffCompression.Lzw", чтобы применить LZW‑сжатие.
# Установите свойство "TiffCompression" в "TiffCompression.Ccitt3", чтобы применить CCITT3‑сжатие.
# Установите свойство "TiffCompression" в "TiffCompression.Ccitt4", чтобы применить CCITT4‑сжатие.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

