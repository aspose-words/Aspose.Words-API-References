---
title: ImageSaveOptions.tiff_compression property
linktitle: tiff_compression property
articleTitle: tiff_compression property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.tiff_compression property. Gets or sets the type of compression to apply when saving generated images to the TIFF format."
type: docs
weight: 170
url: /ar/python-net/aspose.words.saving/imagesaveoptions/tiff_compression/
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
# أنشئ كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
# اضبط خاصية "TiffCompression" إلى "TiffCompression.None" لتطبيق عدم ضغط أثناء الحفظ،
# مما قد ينتج ملف إخراج كبير جداً.
# اضبط خاصية "TiffCompression" إلى "TiffCompression.Rle" لتطبيق ضغط RLE
# اضبط خاصية "TiffCompression" إلى "TiffCompression.Lzw" لتطبيق ضغط LZW.
# اضبط خاصية "TiffCompression" إلى "TiffCompression.Ccitt3" لتطبيق ضغط CCITT3.
# اضبط خاصية "TiffCompression" إلى "TiffCompression.Ccitt4" لتطبيق ضغط CCITT4.
options.tiff_compression = tiff_compression
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.TiffImageCompression.tiff', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

