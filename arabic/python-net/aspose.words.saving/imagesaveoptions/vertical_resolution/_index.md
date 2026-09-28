---
title: ImageSaveOptions.vertical_resolution property
linktitle: vertical_resolution property
articleTitle: vertical_resolution property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.vertical_resolution property. Gets or sets the vertical resolution for the generated images, in dots per inch."
type: docs
weight: 190
url: /ar/python-net/aspose.words.saving/imagesaveoptions/vertical_resolution/
---

## ImageSaveOptions.vertical_resolution property

Gets or sets the vertical resolution for the generated images, in dots per inch.


```python
@property
def vertical_resolution(self) -> float:
    ...

@vertical_resolution.setter
def vertical_resolution(self, value: float):
    ...

```

### Remarks

This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.




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

