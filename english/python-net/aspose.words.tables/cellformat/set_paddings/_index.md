---
title: CellFormat.set_paddings method
linktitle: set_paddings method
articleTitle: set_paddings method
second_title: Aspose.Words for Python
description: "CellFormat.set_paddings method. Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell."
type: docs
weight: 170
url: /python-net/aspose.words.tables/cellformat/set_paddings/
---

## set_paddings(left_padding, top_padding, right_padding, bottom_padding) {#float_float_float_float}

Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.


```python
def set_paddings(self, left_padding: float, top_padding: float, right_padding: float, bottom_padding: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| left_padding | float |  |
| top_padding | float |  |
| right_padding | float |  |
| bottom_padding | float |  |

### Examples

Shows how to pad the contents of a cell with whitespace.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Set a padding distance (in points) between the border and the text contents
# of each table cell we create with the document builder.
builder.cell_format.set_paddings(5, 10, 40, 50)
# Create a table with one cell whose contents will have whitespace padding.
builder.start_table()
builder.insert_cell()
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.Padding.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

