---
title: CellFormat.right_padding property
linktitle: right_padding property
articleTitle: right_padding property
second_title: Aspose.Words for Python
description: "CellFormat.right_padding property. Returns or sets the amount of space (in points) to add to the right of the contents of cell."
type: docs
weight: 90
url: /ar/python-net/aspose.words.tables/cellformat/right_padding/
---

## CellFormat.right_padding property

Returns or sets the amount of space (in points) to add to the right of the contents of cell.


```python
@property
def right_padding(self) -> float:
    ...

@right_padding.setter
def right_padding(self, value: float):
    ...

```

### Examples

Shows how to format cells with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# أدرج خلية ثانية، ثم قم بتكوين خيارات الحشو النصي للخلية.
# المُنشئ سيطبق هذه الإعدادات على خليةه الحالية، وأي خلايا جديدة تُنشأ بعد ذلك.
builder.insert_cell()
cell_format = builder.cell_format
cell_format.width = 250
cell_format.left_padding = 30
cell_format.right_padding = 30
cell_format.top_padding = 30
cell_format.bottom_padding = 30
builder.write('Row 1, cell 2.')
builder.end_row()
builder.end_table()
# الخلية الأولى لم تتأثر بإعادة تكوين الحشو، ولا تزال تحتفظ بالقيم الافتراضية.
self.assertEqual(0, table.first_row.cells[0].cell_format.width)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.left_padding)
self.assertEqual(5.4, table.first_row.cells[0].cell_format.right_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.top_padding)
self.assertEqual(0, table.first_row.cells[0].cell_format.bottom_padding)
self.assertEqual(250, table.first_row.cells[1].cell_format.width)
self.assertEqual(30, table.first_row.cells[1].cell_format.left_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.right_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.top_padding)
self.assertEqual(30, table.first_row.cells[1].cell_format.bottom_padding)
# ستظل الخلية الأولى تنمو في مستند الإخراج لتطابق حجم الخلية المجاورة لها.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetCellFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

