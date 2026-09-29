---
title: SaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "SaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used."
type: docs
weight: 110
url: /it/python-net/aspose.words.saving/saveoptions/save_format/
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
# Usa un oggetto SaveOptions per specificare la codifica di un documento che salveremo.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Per impostazione predefinita, un documento .epub di output avrà tutti i suoi contenuti in un'unica parte HTML.
# Un criterio di divisione ci consente di segmentare il documento in diverse parti HTML.
# Imposteremo i criteri per dividere il documento in paragrafi di intestazione.
# Ciò è utile per i lettori che non possono leggere file HTML più grandi di una dimensione specifica.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Specifica che vogliamo esportare le proprietà del documento.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

