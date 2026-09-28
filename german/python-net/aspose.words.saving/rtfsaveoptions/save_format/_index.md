---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /de/python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Erstellen Sie ein "RtfSaveOptions"-Objekt, das Sie an die "Save"-Methode des Dokuments übergeben, um zu ändern, wie wir es als RTF speichern.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# Setzen Sie die Eigenschaft "ExportCompactSize" auf "true", um
# die Größe des gespeicherten Dokuments zu reduzieren, allerdings auf Kosten der Kompatibilität für Rechts-nach-Links-Text.
options.export_compact_size = True
# Setzen Sie die Eigenschaft "ExportImagesFotOldReaders" auf "true", um zusätzliche Schlüsselwörter zu verwenden, damit unser Dokument
# mit Lesern vor Microsoft Word 97 und WordPad kompatibel ist.
# Setzen Sie die Eigenschaft "ExportImagesFotOldReaders" auf "false", um die Größe des Dokuments zu reduzieren,
# jedoch verhindern, dass alte Leser nicht‑Metadatei‑ oder BMP‑Bilder, die das Dokument enthalten könnte, lesen können.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

