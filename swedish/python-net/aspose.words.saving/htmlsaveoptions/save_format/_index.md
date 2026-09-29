---
title: HtmlSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 460
url: /sv/python-net/aspose.words.saving/htmlsaveoptions/save_format/
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
# Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Som standard kommer ett genererat .epub-dokument att ha allt innehåll i en HTML-del.
# Ett delningskriterium gör det möjligt att segmentera dokumentet i flera HTML-delar.
# Vi kommer att ställa in kriterierna för att dela dokumentet i rubrikparagrafer.
# Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Ange att vi vill exportera dokumentegenskaper.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

