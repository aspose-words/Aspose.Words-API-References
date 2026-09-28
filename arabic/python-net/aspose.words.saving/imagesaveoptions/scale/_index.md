---
title: ImageSaveOptions.scale property
linktitle: scale property
articleTitle: scale property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.scale property. Gets or sets the zoom factor for the generated images."
type: docs
weight: 140
url: /ar/python-net/aspose.words.saving/imagesaveoptions/scale/
---

## ImageSaveOptions.scale property

Gets or sets the zoom factor for the generated images.


```python
@property
def scale(self) -> float:
    ...

@scale.setter
def scale(self, value: float):
    ...

```

### Remarks

The default value is 1.0. The value must be greater than 0.


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

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# أنشئ كائن "ImageSaveOptions" لتمريره إلى طريقة "Save" الخاصة بمُصوِّر العقد لتعديل
# كيفية تحويل عقدة OfficeMath إلى صورة.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# عيّن الخاصية "Scale" إلى 5 لتصوير الكائن بمقدار خمسة أضعاف حجمه الأصلي.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

