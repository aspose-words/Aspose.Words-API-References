---
title: ImageSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.save_format property. Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used"
type: docs
weight: 130
url: /ar/python-net/aspose.words.saving/imagesaveoptions/save_format/
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
# عند حفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
# تحرير الصورة أثناء قيام عملية الحفظ بتصييرها.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# يمكننا تعديل هذه الخصائص لتغيير سطوع الصورة وتباينها.
# كلاهما على مقياس من 0 إلى 1 ويكونان عند 0.5 افتراضيًا.
options.image_brightness = 0.3
options.image_contrast = 0.7
# يمكننا تعديل الدقة الأفقية والعمودية باستخدام هذه الخصائص.
# سيؤثر ذلك على أبعاد الصورة.
# القيمة الافتراضية لهذه الخصائص هي 96.0، لدقة 96 نقطة في البوصة.
options.horizontal_resolution = 72
options.vertical_resolution = 72
# يمكننا تحجيم الصورة باستخدام هذه الخاصية. القيمة الافتراضية هي 1.0، لتكبير بنسبة 100٪.
# يمكننا استخدام هذه الخاصية لإلغاء أي تغييرات في أبعاد الصورة قد يسببها تغيير الدقة.
options.scale = 96 / 72
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.EditImage.png', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

