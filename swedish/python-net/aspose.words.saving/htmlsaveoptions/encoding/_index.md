---
title: HtmlSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML, MHTML or EPUB"
type: docs
weight: 100
url: /sv/python-net/aspose.words.saving/htmlsaveoptions/encoding/
---

## HtmlSaveOptions.encoding property

Specifies the encoding to use when exporting to HTML, MHTML or EPUB.
Default value is ``new UTF8Encoding(false)`` (UTF-8 without BOM).



```python
@property
def encoding(self) -> str:
    ...

@encoding.setter
def encoding(self, value: str):
    ...

```

### Remarks




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

