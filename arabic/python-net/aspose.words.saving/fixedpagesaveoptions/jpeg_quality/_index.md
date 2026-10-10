---
title: FixedPageSaveOptions.jpeg_quality property
linktitle: jpeg_quality property
articleTitle: jpeg_quality property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.jpeg_quality property. Gets or sets a value determining the quality of the JPEG images inside Html document."
type: docs
weight: 20
url: /ar/python-net/aspose.words.saving/fixedpagesaveoptions/jpeg_quality/
---

## FixedPageSaveOptions.jpeg_quality property

Gets or sets a value determining the quality of the JPEG images inside Html document.


```python
@property
def jpeg_quality(self) -> int:
    ...

@jpeg_quality.setter
def jpeg_quality(self, value: int):
    ...

```

### Remarks

Has effect only when a document contains JPEG images.

Use this property to get or set the quality of the images inside a document when saving in fixed page format.
The value may vary from 0 to 100 where 0 means worst quality but maximum compression and 100
means best quality but minimum compression.

The default value is 95.




### Examples

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# أنشئ كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# قم بتعيين الخاصية "JpegQuality" إلى "10" لاستخدام ضغط أقوى عند عرض المستند.
# سيؤدي ذلك إلى تقليل حجم ملف المستند، لكن الصورة ستظهر عيوب ضغط أكثر وضوحًا.
image_options.jpeg_quality = 10
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighCompression.jpg', save_options=image_options)
# قم بتعيين الخاصية "JpegQuality" إلى "100" لاستخدام ضغط أضعف عند عرض المستند.
# سيحسن هذا جودة الصورة على حساب زيادة حجم الملف.
image_options.jpeg_quality = 100
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.JpegQuality.HighQuality.jpg', save_options=image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

