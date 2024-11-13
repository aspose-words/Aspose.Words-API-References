---
title: TxtSaveOptions.preserve_table_layout property
linktitle: preserve_table_layout property
articleTitle: preserve_table_layout property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.preserve_table_layout property. Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format"
type: docs
weight: 50
url: /python-net/aspose.words.saving/txtsaveoptions/preserve_table_layout/
---

## TxtSaveOptions.preserve_table_layout property

Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format.
The default value is ``False``.



```python
@property
def preserve_table_layout(self) -> bool:
    ...

@preserve_table_layout.setter
def preserve_table_layout(self, value: bool):
    ...

```

### Examples

Shows how to preserve the layout of tables when converting to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1')
builder.insert_cell()
builder.write('Row 1, cell 2')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, cell 1')
builder.insert_cell()
builder.write('Row 2, cell 2')
builder.end_table()
# Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
# to modify how we save the document to plaintext.
txt_save_options = aw.saving.TxtSaveOptions()
# Set the "PreserveTableLayout" property to "true" to apply whitespace padding to the contents
# of the output plaintext document to preserve as much of the table's layout as possible.
# Set the "PreserveTableLayout" property to "false" to save all tables' contents
# as a continuous body of text, with just a new line for each row.
txt_save_options.preserve_table_layout = preserve_table_layout
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PreserveTableLayout.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.PreserveTableLayout.txt')
if preserve_table_layout:
    self.assertEqual('Row 1, cell 1                                           Row 1, cell 2\r\n' + 'Row 2, cell 1                                           Row 2, cell 2\r\n\r\n', doc_text)
else:
    self.assertEqual('Row 1, cell 1\r' + 'Row 1, cell 2\r' + 'Row 2, cell 1\r' + 'Row 2, cell 2\r\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

