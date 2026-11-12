---
title: HtmlSaveOptions.export_document_properties property
linktitle: export_document_properties property
articleTitle: export_document_properties property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_document_properties property. Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB"
type: docs
weight: 120
url: /ru/python-net/aspose.words.saving/htmlsaveoptions/export_document_properties/
---

## HtmlSaveOptions.export_document_properties property

Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB.
Default value is ``False``.



```python
@property
def export_document_properties(self) -> bool:
    ...

@export_document_properties.setter
def export_document_properties(self, value: bool):
    ...

```

### Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Используйте объект SaveOptions, чтобы указать кодировку для документа, который мы будем сохранять.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# По умолчанию выходной .epub‑документ будет содержать всё своё содержимое в одной HTML‑части.
# Критерий разбиения позволяет нам сегментировать документ на несколько HTML‑частей.
# Мы установим критерий разбиения документа на абзацы заголовков.
# Это полезно для читателей, которые не могут читать HTML‑файлы, превышающие определённый размер.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Укажите, что мы хотим экспортировать свойства документа.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

