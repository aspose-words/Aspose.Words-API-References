---
title: Table.left_indent property
linktitle: left_indent property
articleTitle: left_indent property
second_title: Aspose.Words for Python
description: "Table.left_indent property. Gets or sets the value that represents the left indent of the table."
type: docs
weight: 190
url: /ar/python-net/aspose.words.tables/table/left_indent/
---

## Table.left_indent property

Gets or sets the value that represents the left indent of the table.


```python
@property
def left_indent(self) -> float:
    ...

@left_indent.setter
def left_indent(self, value: float):
    ...

```

### Examples

Shows how to create a formatted table using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
table.left_indent = 20
# تعيين بعض خيارات التنسيق للنص ومظهر الجدول.
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.from_argb(198, 217, 241)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = 'Arial'
builder.font.bold = True
# تكوين خيارات التنسيق في منشئ المستند سيطبقها
# على الخلية/الصف الحالي الذي يقع فيه مؤشره،
# وكذلك أي خلايا وصفوف جديدة تُنشأ باستخدام ذلك المنشئ.
builder.write('Header Row,\n Cell 1')
builder.insert_cell()
builder.write('Header Row,\n Cell 2')
builder.insert_cell()
builder.write('Header Row,\n Cell 3')
builder.end_row()
# إعادة تكوين كائنات تنسيق المنشئ للصفوف والخلايا الجديدة التي نحن على وشك إنشائها.
# المنشئ لن يطبق هذه على الصف الأول الذي تم إنشاؤه بالفعل حتى يبرز كصف رأس.
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.white
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.row_format.height = 30
builder.row_format.height_rule = aw.HeightRule.AUTO
builder.insert_cell()
builder.font.size = 12
builder.font.bold = False
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
builder.insert_cell()
builder.write('Row 1, Cell 3.')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.insert_cell()
builder.write('Row 2, Cell 3.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateFormattedTable.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

