---
title: DownsampleOptions.resolution property
linktitle: resolution property
articleTitle: resolution property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution property. Specifies the resolution in pixels per inch which the images should be downsampled to."
type: docs
weight: 30
url: /ar/python-net/aspose.words.saving/downsampleoptions/resolution/
---

## DownsampleOptions.resolution property

Specifies the resolution in pixels per inch which the images should be downsampled to.


```python
@property
def resolution(self) -> int:
    ...

@resolution.setter
def resolution(self, value: int):
    ...

```

### Remarks

The default value is 220 ppi.


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

