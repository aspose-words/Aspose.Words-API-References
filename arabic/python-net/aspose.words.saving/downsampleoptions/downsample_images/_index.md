---
title: DownsampleOptions.downsample_images property
linktitle: downsample_images property
articleTitle: downsample_images property
second_title: Aspose.Words for Python
description: "DownsampleOptions.downsample_images property. Specifies whether images should be downsampled."
type: docs
weight: 20
url: /ar/python-net/aspose.words.saving/downsampleoptions/downsample_images/
---

## DownsampleOptions.downsample_images property

Specifies whether images should be downsampled.


```python
@property
def downsample_images(self) -> bool:
    ...

@downsample_images.setter
def downsample_images(self, value: bool):
    ...

```

### Remarks

The default value is ``True``.



### Examples

Shows how to change the resolution of images in the PDF document.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# بشكل افتراضي، تقوم Aspose.Words بتقليل دقة جميع الصور في المستند الذي نحفظه كملف PDF إلى 220 نقطة في البوصة.
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# قم بتعيين الخاصية "Resolution" إلى "36" لتقليل دقة جميع الصور إلى 36 نقطة في البوصة.
options.downsample_options.resolution = 36
# قم بتعيين الخاصية "ResolutionThreshold" لتطبيق تقليل الدقة فقط على
# الصور التي تكون دقتها أعلى من 128 نقطة في البوصة.
options.downsample_options.resolution_threshold = 128
# سيتم تقليل دقة الصورتين الأوليتين فقط من المستند في هذه المرحلة.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

