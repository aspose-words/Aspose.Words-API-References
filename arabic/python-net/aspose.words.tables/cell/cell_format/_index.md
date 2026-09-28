---
title: Cell.cell_format property
linktitle: cell_format property
articleTitle: cell_format property
second_title: Aspose.Words for Python
description: "Cell.cell_format property. Provides access to the formatting properties of the cell."
type: docs
weight: 20
url: /ar/python-net/aspose.words.tables/cell/cell_format/
---

## Cell.cell_format property

Provides access to the formatting properties of the cell.


```python
@property
def cell_format(self) -> aspose.words.tables.CellFormat:
    ...

```

### Examples

Shows how to modify the format of rows and cells in a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('City')
builder.insert_cell()
builder.write('Country')
builder.end_row()
builder.insert_cell()
builder.write('London')
builder.insert_cell()
builder.write('U.K.')
builder.end_table()
# استخدم خاصية "RowFormat" للصف الأول لتعديل التنسيق
# لمحتويات جميع الخلايا في هذا الصف.
row_format = table.first_row.row_format
row_format.height = 25
row_format.borders.get_by_border_type(aw.BorderType.BOTTOM).color = aspose.pydrawing.Color.red
# استخدم خاصية "CellFormat" للخلية الأولى في الصف الأخير لتعديل تنسيق محتويات تلك الخلية.
cell_format = table.last_row.first_cell.cell_format
cell_format.width = 100
cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
doc.save(file_name=ARTIFACTS_DIR + 'Table.RowCellFormat.docx')
```

Shows how to modify formatting of a table cell.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
first_cell = table.first_row.first_cell
# استخدم خاصية "CellFormat" للخلية لتعيين التنسيق الذي يغيّر مظهر تلك الخلية.
first_cell.cell_format.width = 30
first_cell.cell_format.orientation = aw.TextOrientation.DOWNWARD
first_cell.cell_format.shading.foreground_pattern_color = aspose.pydrawing.Color.light_green
doc.save(file_name=ARTIFACTS_DIR + 'Table.CellFormat.docx')
```

Shows how to combine the rows from two tables into one.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
# فيما يلي طريقتان للحصول على جدول من مستند.
# 1 -  من مجموعة "Tables" لعقدة Body:
first_table = doc.first_section.body.tables[0]
# 2 -  باستخدام طريقة "GetChild":
second_table = doc.get_child(aw.NodeType.TABLE, 1, True).as_table()
# إلحاق جميع الصفوف من الجدول الحالي إلى التالي.
while second_table.has_child_nodes:
    first_table.rows.add(second_table.first_row)
# إزالة حاوية الجدول الفارغة.
second_table.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Table.CombineTables.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Cell](../)

