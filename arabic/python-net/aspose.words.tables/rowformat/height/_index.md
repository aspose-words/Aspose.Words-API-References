---
title: RowFormat.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "RowFormat.height property. Gets or sets the height of the table row in points."
type: docs
weight: 40
url: /ar/python-net/aspose.words.tables/rowformat/height/
---

## RowFormat.height property

Gets or sets the height of the table row in points.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
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

Shows how to format rows with a document builder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1.')
# ابدأ صفًا ثانيًا، ثم اضبط ارتفاعه. سيطبق المُنشئ هذه الإعدادات على
# صفه الحالي، بالإضافة إلى أي صفوف جديدة ينشئها لاحقًا.
builder.end_row()
row_format = builder.row_format
row_format.height = 100
row_format.height_rule = aw.HeightRule.EXACTLY
builder.insert_cell()
builder.write('Row 2, cell 1.')
builder.end_table()
# الصف الأول لم يتأثر بإعادة تكوين الحشو ولا يزال يحتفظ بالقيم الافتراضية.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SetRowFormatting.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

