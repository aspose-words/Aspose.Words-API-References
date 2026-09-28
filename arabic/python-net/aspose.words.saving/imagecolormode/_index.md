---
title: ImageColorMode enumeration
linktitle: ImageColorMode enumeration
articleTitle: ImageColorMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageColorMode enumeration. Specifies the color mode for the generated images of document pages."
type: docs
weight: 380
url: /ar/python-net/aspose.words.saving/imagecolormode/
---

## ImageColorMode enumeration

Specifies the color mode for the generated images of document pages.


### Members

| Name | Description |
| --- | --- |
| NONE | The pages of the document will be rendered as color images. |
| GRAYSCALE | The pages of the document will be rendered as grayscale images. |
| BLACK_AND_WHITE | The pages of the document will be rendered as black and white images. |

### Examples

Shows how to set a color mode when rendering documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world!')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# عند حفظ المستند كصورة، يمكننا تمرير كائن SaveOptions إلى
# اختيار وضع لون للصورة التي سيولدها عملية الحفظ.
# إذا قمنا بتعيين الخاصية "ImageColorMode" إلى "ImageColorMode.BlackAndWhite",
# ستطبق عملية الحفظ تقليل اللون إلى تدرج الرمادي أثناء تصيير المستند.
# إذا قمنا بتعيين الخاصية "ImageColorMode" إلى "ImageColorMode.Grayscale",
# ستقوم عملية الحفظ بتصيير المستند إلى صورة أحادية اللون.
# إذا قمنا بتعيين الخاصية "ImageColorMode" إلى "None»، فإن عملية الحفظ ستطبق الطريقة الافتراضية
# وستحافظ على جميع ألوان المستند في صورة الإخراج.
image_save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
image_save_options.image_color_mode = image_color_mode
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ColorMode.png', save_options=image_save_options)
```

### See Also

* module [aspose.words.saving](../)

