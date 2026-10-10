---
title: PdfImageColorSpaceExportMode enumeration
linktitle: PdfImageColorSpaceExportMode enumeration
articleTitle: PdfImageColorSpaceExportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfImageColorSpaceExportMode enumeration. Specifies how the color space will be selected for the images in PDF document."
type: docs
weight: 700
url: /ar/python-net/aspose.words.saving/pdfimagecolorspaceexportmode/
---

## PdfImageColorSpaceExportMode enumeration

Specifies how the color space will be selected for the images in PDF document.


### Members

| Name | Description |
| --- | --- |
| AUTO | Aspose.Words automatically selects the most appropriate color space for each image. |
| SIMPLE_CMYK | Aspose.Words coverts RGB images to CMYK color space using simple formula. |

### Examples

Shows how to set a different color space for images in a document as we export it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jpeg image:')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_paragraph()
builder.writeln('Png image:')
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
pdf_save_options = aw.saving.PdfSaveOptions()
# عيّن الخاصية "ImageColorSpaceExportMode" إلى "PdfImageColorSpaceExportMode.Auto" لجعل Aspose.Words
# تختار تلقائيًا مساحة اللون للصور في المستند الذي يحوله إلى PDF.
# في معظم الحالات، ستكون مساحة اللون RGB.
# قم بتعيين الخاصية "ImageColorSpaceExportMode" إلى "PdfImageColorSpaceExportMode.SimpleCmyk"
# لاستخدام مساحة اللون CMYK لجميع الصور في ملف PDF المحفوظ.
# ستقوم Aspose.Words أيضًا بتطبيق ضغط Flate على جميع الصور وتجاهل قيمة الخاصية "ImageCompression".
pdf_save_options.image_color_space_export_mode = pdf_image_color_space_export_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ImageColorSpaceExportMode.pdf', save_options=pdf_save_options)
```

### See Also

* module [aspose.words.saving](../)

