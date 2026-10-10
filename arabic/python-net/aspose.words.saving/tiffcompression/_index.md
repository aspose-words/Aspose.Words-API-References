---
title: TiffCompression enumeration
linktitle: TiffCompression enumeration
articleTitle: TiffCompression enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.TiffCompression enumeration. Specifies what type of compression to apply when saving page images into a TIFF file."
type: docs
weight: 860
url: /ar/python-net/aspose.words.saving/tiffcompression/
---

## TiffCompression enumeration

Specifies what type of compression to apply when saving page images into a TIFF file.


### Members

| Name | Description |
| --- | --- |
| NONE | Specifies no compression. |
| RLE | Specifies the RLE compression scheme. |
| LZW | Specifies the LZW compression scheme. In Java emulated by Deflate (Zip) compression. |
| CCITT3 | Specifies the CCITT3 compression scheme. |
| CCITT4 | Specifies the CCITT4 compression scheme. |

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

* module [aspose.words.saving](../)

