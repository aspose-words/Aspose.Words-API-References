---
title: OoxmlSaveOptions.keep_legacy_control_chars property
linktitle: keep_legacy_control_chars property
articleTitle: keep_legacy_control_chars property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.keep_legacy_control_chars property. Keeps original representation of legacy control characters."
type: docs
weight: 50
url: /sv/python-net/aspose.words.saving/ooxmlsaveoptions/keep_legacy_control_chars/
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
# När vi sparar dokumentet till ett OOXML-format kan vi skapa ett OoxmlSaveOptions object
# och sedan skicka det till dokumentets sparningsmetod för att ändra hur vi sparar dokumentet.
# Ställ in egenskapen "KeepLegacyControlChars" till "true" för att bevara
# det äldre tecknet "ShortDateTime" vid sparande.
# Ställ in egenskapen "KeepLegacyControlChars" till "false" för att ta bort
# det äldre tecknet "ShortDateTime" från utdata-dokumentet.
so = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
so.keep_legacy_control_chars = keep_legacy_control_chars
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.KeepLegacyControlChars.docx', save_options=so)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.KeepLegacyControlChars.docx')
self.assertEqual('\x13date \\@ "MM/dd/yyyy"\x14\x15\x0c' if keep_legacy_control_chars else '\x1e\x0c', doc.first_section.body.get_text())
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

