---
title: DownsampleOptions.resolution_threshold property
linktitle: resolution_threshold property
articleTitle: resolution_threshold property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution_threshold property. Specifies the threshold resolution in pixels per inch"
type: docs
weight: 40
url: /ar/python-net/aspose.words.saving/downsampleoptions/resolution_threshold/
---

## DownsampleOptions.resolution_threshold property

Specifies the threshold resolution in pixels per inch.
If resolution of an image in the document is less than threshold value,
the downsampling algorithm will not be applied.
A value of 0 means the threshold check is not used and all images that can be reduced in size are downsampled.


```python
@property
def resolution_threshold(self) -> int:
    ...

@resolution_threshold.setter
def resolution_threshold(self, value: int):
    ...

```

### Remarks

The default value is 0.


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

