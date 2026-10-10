---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /ru/python-net/aspose.words.saving/tiffcompression/
---

## TiffCompression enumeration

Specifies what type of compression to apply when saving page images into a TIFF file.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies no compression. |
| RLE | Specifies the RLE compression scheme. |
| LZW | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| CCITT3 | Specifies the CCITT3 compression scheme. |
| CCITT4 | Specifies the CCITT4 compression scheme. |

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

* module [aspose.words.saving](../)

