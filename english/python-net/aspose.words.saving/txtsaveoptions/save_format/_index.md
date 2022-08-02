---
title: save_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 60
url: /python-net/aspose.words.saving/txtsaveoptions/save_format/
---

## TxtSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.TEXT](../../../aspose.words/saveformat/#TEXT).



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
* class [TxtSaveOptions](../)

