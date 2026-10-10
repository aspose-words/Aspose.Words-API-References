---
title: OoxmlSaveOptions.keep_legacy_control_chars property
linktitle: keep_legacy_control_chars property
articleTitle: keep_legacy_control_chars property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.keep_legacy_control_chars property. Keeps original representation of legacy control characters."
type: docs
weight: 50
url: /it/python-net/aspose.words.saving/ooxmlsaveoptions/keep_legacy_control_chars/
---

## OoxmlSaveOptions.keep_legacy_control_chars property

Keeps original representation of legacy control characters.


```python
@property
def keep_legacy_control_chars(self) -> bool:
    ...

@keep_legacy_control_chars.setter
def keep_legacy_control_chars(self, value: bool):
    ...

```

### Examples

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

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

