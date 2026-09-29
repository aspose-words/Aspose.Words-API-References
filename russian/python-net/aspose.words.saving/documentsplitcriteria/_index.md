---
title: DocumentSplitCriteria enumeration
linktitle: DocumentSplitCriteria enumeration
articleTitle: DocumentSplitCriteria enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DocumentSplitCriteria enumeration. Specifies how the document is split into parts when saving to [SaveFormat.HTML](../../aspose.words/saveformat/#HTML), [SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3) format."
type: docs
weight: 140
url: /ru/python-net/aspose.words.saving/documentsplitcriteria/
---

## DocumentSplitCriteria enumeration

Specifies how the document is split into parts when saving to [SaveFormat.HTML](../../aspose.words/saveformat/#HTML),
[SaveFormat.EPUB](../../aspose.words/saveformat/#EPUB) or [SaveFormat.AZW3](../../aspose.words/saveformat/#AZW3) format.


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document
at page breaks and heading paragraphs in the same export operation.

Different criteria can partially overlap. For instance, **Heading 1** style is frequently given 
[ParagraphFormat.page_break_before](../../aspose.words/paragraphformat/page_break_before/) property so it falls under two criteria: [DocumentSplitCriteria.PAGE_BREAK](./#PAGE_BREAK) and 
[DocumentSplitCriteria.HEADING_PARAGRAPH](./#HEADING_PARAGRAPH). Some section breaks can cause page breaks and so on. 
In typical cases specifying only one flag is the most practical option.




### Members

| Name | Description |
| --- | --- |
| NONE | The document is not split. |
| PAGE_BREAK | The document is split into parts at explicit page breaks. A page break can be specified by a [ControlChar.PAGE_BREAK](../../aspose.words/controlchar/PAGE_BREAK/) character,  a section break specifying start of new section on a new page, or a paragraph that has its [ParagraphFormat.page_break_before](../../aspose.words/paragraphformat/page_break_before/) property set to ``True``. |
| COLUMN_BREAK | The document is split into parts at column breaks. A column break can be specified by a [ControlChar.COLUMN_BREAK](../../aspose.words/controlchar/COLUMN_BREAK/) character or a section break specifying start of new section in a new column. |
| SECTION_BREAK | The document is split into parts at a section break of any type. |
| HEADING_PARAGRAPH | The document is split into parts at a paragraph formatted using a heading style **Heading 1**, **Heading 2** etc.  Use together with [HtmlSaveOptions.document_split_heading_level](../htmlsaveoptions/document_split_heading_level/) to specify the heading levels  (from 1 to the specified level) at which to split. |

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

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.document_split_criteria](../htmlsaveoptions/document_split_criteria/)

