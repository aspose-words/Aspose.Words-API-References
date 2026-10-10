---
title: ImageSaveOptions.image_brightness property
linktitle: image_brightness property
articleTitle: image_brightness property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.image_brightness property. Gets or sets the brightness for the generated images."
type: docs
weight: 30
url: /ar/python-net/aspose.words.saving/imagesaveoptions/image_brightness/
---

## ImageSaveOptions.image_brightness property

Gets or sets the brightness for the generated images.


```python
@property
def image_brightness(self) -> float:
    ...

@image_brightness.setter
def image_brightness(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats.

The default value is 0.5. The value must be in the range between 0 and 1.




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

