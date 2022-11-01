---
title: preserve_table_layout property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format"
type: docs
weight: 50
url: /python-net/aspose.words.saving/txtsaveoptions/preserve_table_layout/
---

## TxtSaveOptions.preserve_table_layout property

Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format.
The default value is ``False``.



### Examples

Shows how to preserve the layout of tables when converting to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.start_table()
builder.insert_cell()
builder.write("Row 1, cell 1")
builder.insert_cell()
builder.write("Row 1, cell 2")
builder.end_row()
builder.insert_cell()
builder.write("Row 2, cell 1")
builder.insert_cell()
builder.write("Row 2, cell 2")
builder.end_table()

# Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()

# Set the "preserve_table_layout" property to "True" to apply whitespace padding to the contents
# of the output plaintext document to preserve as much of the table's layout as possible.
# Set the "preserve_table_layout" property to "False" to save all tables' contents
# as a continuous body of text, with just a new line for each row.
txt_save_options.preserve_table_layout = preserve_table_layout

doc.save(ARTIFACTS_DIR + "TxtSaveOptions.preserve_table_layout.txt", txt_save_options)

with open(ARTIFACTS_DIR + "TxtSaveOptions.preserve_table_layout.txt", "rb") as file:
    doc_text = file.read().decode("utf-8-sig")

if preserve_table_layout:
    self.assertEqual(
        "Row 1, cell 1                                           Row 1, cell 2\r\n" +
        "Row 2, cell 1                                           Row 2, cell 2\r\n\r\n", doc_text)
else:
    self.assertEqual(
        "Row 1, cell 1\r" +
        "Row 1, cell 2\r" +
        "Row 2, cell 1\r" +
        "Row 2, cell 2\r\r\n", doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

