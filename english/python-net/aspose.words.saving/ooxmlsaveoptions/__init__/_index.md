---
title: OoxmlSaveOptions constructor
linktitle: OoxmlSaveOptions constructor
articleTitle: OoxmlSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.OoxmlSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/ooxmlsaveoptions/__init__/
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
doc = aw.Document(MY_DIR + 'Legacy control character.doc')
# When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
# and then pass it to the document's saving method to modify how we save the document.
# Set the "keep_legacy_control_chars" property to "True" to preserve
# the "ShortDateTime" legacy character while saving.
# Set the "keep_legacy_control_chars" property to "False" to remove
# the "ShortDateTime" legacy character from the output document.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.keep_legacy_control_chars = keep_legacy_control_chars
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.keep_legacy_control_chars.docx', save_options)
doc = aw.Document(ARTIFACTS_DIR + 'OoxmlSaveOptions.keep_legacy_control_chars.docx')
self.assertEqual('\x13date \\@ "d/MM/yyyy"\x14\x15\x0c' if keep_legacy_control_chars else '\x1e\x0c', doc.first_section.body.get_text())
```

## See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

