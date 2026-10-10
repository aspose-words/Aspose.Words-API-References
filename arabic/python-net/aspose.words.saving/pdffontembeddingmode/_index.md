---
title: PdfFontEmbeddingMode enumeration
linktitle: PdfFontEmbeddingMode enumeration
articleTitle: PdfFontEmbeddingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfFontEmbeddingMode enumeration. Specifies how Aspose.Words should embed fonts."
type: docs
weight: 690
url: /ar/python-net/aspose.words.saving/pdffontembeddingmode/
---

## PdfFontEmbeddingMode enumeration

Specifies how Aspose.Words should embed fonts.


### Members

| Name | Description |
| --- | --- |
| EMBED_ALL | Aspose.Words embeds all fonts. |
| EMBED_NONSTANDARD | Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. Only Arial and Times New Roman fonts are affected in this mode because MS Word doesn't embed only these fonts when saving document to PDF. |
| EMBED_NONE | Aspose.Words do not embed any fonts. |

### Examples

Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# "Arial" هو خط قياسي، و"Courier New" هو خط غير قياسي.
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Courier New'
builder.writeln('The quick brown fox jumps over the lazy dog.')
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# تعيين خاصية "EmbedFullFonts" إلى "true" لتضمين كل حرف من كل خط مضمّن في ملف PDF الناتج.
options.embed_full_fonts = True
# تعيين خاصية "FontEmbeddingMode" إلى "EmbedAll" لتضمين جميع الخطوط في ملف PDF الناتج.
# تعيين خاصية "FontEmbeddingMode" إلى "EmbedNonstandard" للسماح فقط بتضمين الخطوط غير القياسية في ملف PDF الناتج.
# تعيين خاصية "FontEmbeddingMode" إلى "EmbedNone" لعدم تضمين أي خطوط في ملف PDF الناتج.
options.font_embedding_mode = pdf_font_embedding_mode
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EmbedWindowsFonts.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

