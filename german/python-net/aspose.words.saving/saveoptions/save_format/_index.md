---
title: SaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "SaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used."
type: docs
weight: 110
url: /de/python-net/aspose.words.saving/saveoptions/save_format/
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
# Verwende ein SaveOptions-Objekt, um die Kodierung für ein Dokument festzulegen, das wir speichern werden.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = system_helper.text.Encoding.utf_8()
# Standardmäßig enthält ein ausgegebenes .epub-Dokument alle Inhalte in einem einzigen HTML-Teil.
# Ein Trennkriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
# Wir werden das Kriterium festlegen, um das Dokument in Überschriftsabsätze zu splitten.
# Dies ist nützlich für Leser, die HTML-Dateien, die größer als eine bestimmte Größe sind, nicht lesen können.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH
# Gib an, dass wir Dokumenteneigenschaften exportieren möchten.
save_options.export_document_properties = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.Doc2EpubSaveOptions.epub', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

