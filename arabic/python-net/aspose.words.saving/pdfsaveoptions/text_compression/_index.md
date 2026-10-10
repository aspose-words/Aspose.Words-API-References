---
title: PdfSaveOptions.text_compression property
linktitle: text_compression property
articleTitle: text_compression property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.text_compression property. Specifies compression type to be used for all textual content in the document."
type: docs
weight: 330
url: /ar/python-net/aspose.words.saving/pdfsaveoptions/text_compression/
---

## PdfSaveOptions.text_compression property

Specifies compression type to be used for all textual content in the document.


```python
@property
def text_compression(self) -> aspose.words.saving.PdfTextCompression:
    ...

@text_compression.setter
def text_compression(self, value: aspose.words.saving.PdfTextCompression):
    ...

```

### Remarks

Default is [PdfTextCompression.FLATE](../../pdftextcompression/#FLATE).

Significantly increases output size when saving a document without compression.




### Examples

Shows how to apply text compression when saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 100:
    builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    i += 1
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# عيّن خاصية "TextCompression" إلى "PdfTextCompression.None" لعدم تطبيق أي
# ضغط على النص عند حفظ المستند إلى PDF.
# عيّن خاصية "TextCompression" إلى "PdfTextCompression.Flate" لتطبيق ضغط ZIP
# على النص عند حفظ المستند إلى PDF. كلما كان المستند أكبر، زاد الأثر الذي سيحدثه ذلك.
options.text_compression = pdf_text_compression
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.TextCompression.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

