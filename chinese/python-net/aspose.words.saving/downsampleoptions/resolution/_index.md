---
title: DownsampleOptions.resolution property
linktitle: resolution property
articleTitle: resolution property
second_title: Aspose.Words for Python
description: "DownsampleOptions.resolution property. Specifies the resolution in pixels per inch which the images should be downsampled to."
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/downsampleoptions/resolution/
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
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 默认情况下，Aspose.Words 会将我们保存为 PDF 的文档中的所有图像下采样至 220 ppi。
self.assertTrue(options.downsample_options.downsample_images)
self.assertEqual(220, options.downsample_options.resolution)
self.assertEqual(0, options.downsample_options.resolution_threshold)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.Default.pdf', save_options=options)
# 将 "Resolution" 属性设置为 "36"，将所有图像下采样至 36 ppi。
options.downsample_options.resolution = 36
# 将 "ResolutionThreshold" 属性设置为仅对以下情况应用下采样：
# 分辨率高于 128 ppi 的图像。
options.downsample_options.resolution_threshold = 128
# 此阶段仅会对文档中的前两张图像进行下采样。
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DownsampleOptions.LowerResolution.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DownsampleOptions](../)

