---
title: HtmlSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 460
url: /ru/python-net/aspose.words.saving/htmlsaveoptions/save_format/
---

## HtmlSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../../aspose.words/saveformat/#MHTML), [SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB),
[SaveFormat.AZW3](../../../aspose.words/saveformat/#AZW3) or [SaveFormat.MOBI](../../../aspose.words/saveformat/#MOBI).



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

