---
title: OoxmlSaveOptions.keep_legacy_control_chars property
linktitle: keep_legacy_control_chars property
articleTitle: keep_legacy_control_chars property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.keep_legacy_control_chars property. Keeps original representation of legacy control characters."
type: docs
weight: 40
url: /python-net/aspose.words.saving/ooxmlsaveoptions/keep_legacy_control_chars/
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
doc = aw.Document(MY_DIR + "Legacy control character.doc")

# When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
# and then pass it to the document's saving method to modify how we save the document.
# Set the "keep_legacy_control_chars" property to "True" to preserve
# the "ShortDateTime" legacy character while saving.
# Set the "keep_legacy_control_chars" property to "False" to remove
# the "ShortDateTime" legacy character from the output document.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.keep_legacy_control_chars = keep_legacy_control_chars

doc.save(ARTIFACTS_DIR + "OoxmlSaveOptions.keep_legacy_control_chars.docx", save_options)

doc = aw.Document(ARTIFACTS_DIR + "OoxmlSaveOptions.keep_legacy_control_chars.docx")

self.assertEqual(
    "\u0013date \\@ \"d/MM/yyyy\"\u0014\u0015\f" if keep_legacy_control_chars else "\u001e\f",
    doc.first_section.body.get_text())
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

