---
title: HtmlSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML, MHTML or EPUB"
type: docs
weight: 100
url: /de/python-net/aspose.words.saving/htmlsaveoptions/encoding/
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
* class [HtmlSaveOptions](../)

