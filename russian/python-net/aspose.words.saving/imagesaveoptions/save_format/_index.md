---
title: ImageSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.save_format property. Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used"
type: docs
weight: 130
url: /ru/python-net/aspose.words.saving/imagesaveoptions/save_format/
---

## ImageSaveOptions.save_format property

Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used.
Can be a raster
[SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../../aspose.words/saveformat/#BMP),
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG) or vector [SaveFormat.EMF](../../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../../aspose.words/saveformat/#EPS),
[SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P), [SaveFormat.SVG](../../../aspose.words/saveformat/#SVG).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Remarks

The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../) and via [SvgSaveOptions](../../svgsaveoptions/).




### Examples

Shows how to edit the image while Aspose.Words converts a document to one.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# При сохранении документа в виде изображения мы можем передать объект SaveOptions к
# отредактируйте изображение, пока операция сохранения его рендерит.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Мы можем настроить эти свойства, чтобы изменить яркость и контраст изображения.
# Оба находятся в диапазоне от 0 до 1 и по умолчанию равны 0,5.
options.image_brightness = 0.3
options.image_contrast = 0.7
# Мы можем настроить горизонтальное и вертикальное разрешение с помощью этих свойств.
# Это повлияет на размеры изображения.
# Значение по умолчанию для этих свойств равно 96,0 при разрешении 96dpi.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# Мы можем масштабировать изображение, используя это свойство. Значение по умолчанию — 1,0, что соответствует масштабированию 100%.
# Мы можем использовать это свойство, чтобы отменить любые изменения размеров изображения, которые могут возникнуть при изменении разрешения.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

