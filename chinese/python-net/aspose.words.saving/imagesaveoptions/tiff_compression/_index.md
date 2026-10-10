---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /zh/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
---

## ImageSaveOptions.tiff_compression property

Gets or sets the type of compression to apply when saving generated images to the TIFF format.


```python
@property
def tiff_compression(self) -> aspose.words.saving.TiffCompression:
    ...

@tiff_compression.setter
def tiff_compression(self, value: aspose.words.saving.TiffCompression):
    ...

```

### Remarks

Has effect only when saving to TIFF.

The default value is [TiffCompression.LZW](../../tiffcompression/#LZW).




### Examples

Shows how to select the compression scheme to apply to a document that we convert into a TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 创建一个 "ImageSaveOptions" 对象，以便我们传递给文档的 "Save" 方法
# 以修改该方法将文档渲染为图像的方式。
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# 将 "TiffCompression" 属性设置为 "TiffCompression.None"，在保存时不进行压缩，
# 这可能导致输出文件非常大。
# 将 "TiffCompression" 属性设置为 "TiffCompression.Rle"，以应用 RLE 压缩
# 将 "TiffCompression" 属性设置为 "TiffCompression.Lzw"，以应用 LZW 压缩。
# 将 "TiffCompression" 属性设置为 "TiffCompression.Ccitt3"，以应用 CCITT3 压缩。
# 将 "TiffCompression" 属性设置为 "TiffCompression.Ccitt4"，以应用 CCITT4 压缩。
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

