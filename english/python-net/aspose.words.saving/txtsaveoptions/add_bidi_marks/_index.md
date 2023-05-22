---
title: TxtSaveOptions.add_bidi_marks property
linktitle: add_bidi_marks property
articleTitle: add_bidi_marks property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.add_bidi_marks property. Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format."
type: docs
weight: 20
url: /python-net/aspose.words.saving/txtsaveoptions/add_bidi_marks/
---

## TxtSaveOptions.add_bidi_marks property

Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is ``False``.




### Examples

Shows how to insert Unicode Character 'RIGHT-TO-LEFT MARK' (U+200F) before each bi-directional Run in text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")
builder.paragraph_format.bidi = True
builder.writeln("שלום עולם!")
builder.writeln("مرحبا بالعالم!")

# Create a "TxtSaveOptions" object, which we can pass to the document's "save" method
# to modify how we save the document to plaintext.
save_options = aw.saving.TxtSaveOptions()
save_options.encoding = "utf-8"

# Set the "add_bidi_marks" property to "True" to add marks before runs
# with right-to-left text to indicate the fact.
# Set the "add_bidi_marks" property to "False" to write all left-to-right
# and right-to-left run equally with nothing to indicate which is which.
save_options.add_bidi_marks = add_bidi_marks

doc.save(ARTIFACTS_DIR + "TxtSaveOptions.add_bidi_marks.txt", save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.add_bidi_marks.txt", "rb") as file:
    doc_text = file.read().decode('utf-8')

if add_bidi_marks:
    self.assertEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", doc_text)
    self.assertIn("\u200f", doc_text)
else:
    self.assertEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", doc_text)
    self.assertNotIn("\u200f", doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

