---
title: SaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "SaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used."
type: docs
weight: 110
url: /ar/python-net/aspose.words.saving/saveoptions/save_format/
---

## SaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.


```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# استخدم كائن SaveOptions لتحديد الترميز للمستند الذي سنقوم بحفظه.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# بشكل افتراضي، سيحتوي مستند .epub الناتج على جميع محتوياته في جزء HTML واحد.
# معيار التقسيم يتيح لنا تقسيم المستند إلى عدة أجزاء HTML.
# سنحدد المعايير لتقسيم المستند إلى فقرات عناوين.
# هذا مفيد للقراء الذين لا يمكنهم قراءة ملفات HTML التي تتجاوز حجمًا معينًا.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# حدد أننا نريد تصدير خصائص المستند.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

