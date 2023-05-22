---
title: TxtSaveOptionsBase.paragraph_break property
linktitle: paragraph_break property
articleTitle: paragraph_break property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.paragraph_break property. Specifies the string to use as a paragraph break when exporting in text formats."
type: docs
weight: 40
url: /python-net/aspose.words.saving/txtsaveoptionsbase/paragraph_break/
---

## TxtSaveOptionsBase.paragraph_break property

Specifies the string to use as a paragraph break when exporting in text formats.

The default value is [ControlChar.CR_LF](../../../aspose.words/controlchar/CR_LF/).




### Examples

Shows how to save a .txt document with a custom paragraph break.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Paragraph 1.")
builder.writeln("Paragraph 2.")
builder.write("Paragraph 3.")

# Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()

self.assertEqual(aw.SaveFormat.TEXT, txt_save_options.save_format)

# Set the "paragraph_break" to a custom value that we wish to put at the end of every paragraph.
txt_save_options.paragraph_break = " End of paragraph.\n\n\t"

doc.save(ARTIFACTS_DIR + "TxtSaveOptions.paragraph_break.txt", txt_save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.paragraph_break.txt", "rb") as file:
    doc_text = file.read().decode("utf-8-sig")

self.assertEqual(
    "Paragraph 1. End of paragraph.\n\n\t" +
    "Paragraph 2. End of paragraph.\n\n\t" +
    "Paragraph 3. End of paragraph.\n\n\t", doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

