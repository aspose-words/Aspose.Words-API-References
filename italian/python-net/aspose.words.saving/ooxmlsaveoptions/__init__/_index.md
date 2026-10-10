---
title: OoxmlSaveOptions constructor
linktitle: OoxmlSaveOptions constructor
articleTitle: OoxmlSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.OoxmlSaveOptions constructor"
type: docs
weight: 10
url: /it/python-net/aspose.words.saving/ooxmlsaveoptions/__init__/
---

## OoxmlSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX) format.



```python
def __init__(self):
    ...
```

## OoxmlSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX),
[SaveFormat.DOCM](../../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../../aspose.words/saveformat/#DOTM) or
[SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Can be [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX), [SaveFormat.DOCM](../../../aspose.words/saveformat/#DOCM), [SaveFormat.DOTX](../../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../../aspose.words/saveformat/#DOTM) or [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC). |

## Examples

Shows how to support legacy control characters when converting to .docx.

```python
doc = aw.Document(file_name=MY_DIR + 'Legacy control character.doc')
# Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
# e poi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
# Imposta la proprietà "KeepLegacyControlChars" su "true" per preservare
# il carattere legacy "ShortDateTime" durante il salvataggio.
# Imposta la proprietà "KeepLegacyControlChars" su "false" per rimuovere
# il carattere legacy "ShortDateTime" dal documento di output.
so = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
so.keep_legacy_control_chars = keep_legacy_control_chars
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.KeepLegacyControlChars.docx', save_options=so)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.KeepLegacyControlChars.docx')
self.assertEqual('\x13date \\@ "MM/dd/yyyy"\x14\x15\x0c' if keep_legacy_control_chars else '\x1e\x0c', doc.first_section.body.get_text())
```

## See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

