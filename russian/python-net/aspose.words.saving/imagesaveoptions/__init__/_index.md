---
title: ImageSaveOptions constructor
linktitle: ImageSaveOptions constructor
articleTitle: ImageSaveOptions constructor
second_title: Aspose.Words for Python
description: "ImageSaveOptions constructor. Initializes a new instance of this class that can be used to save rendered images in the [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS), [SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format."
type: docs
weight: 10
url: /ru/python-net/aspose.words.saving/imagesaveoptions/__init__/
---

## ImageSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save rendered images in the
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS),
[SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Can be [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS) [SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG) format. |

### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в изображение.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Установите свойство "JpegQuality" в значение "10", чтобы использовать более сильное сжатие при отрисовке документа.
# Это уменьшит размер файла документа, но изображение будет показывать более заметные артефакты сжатия.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# Установите свойство "JpegQuality" в значение "100", чтобы использовать более слабое сжатие при рендеринге документа.
# Это улучшит качество изображения за счёт увеличения размера файла.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

