---
title: DocumentBuilder.row_format property
linktitle: row_format property
articleTitle: row_format property
second_title: Aspose.Words for Python
description: "DocumentBuilder.row_format property. Returns an object that represents current table row formatting properties."
type: docs
weight: 180
url: /ar/python-net/aspose.words/documentbuilder/row_format/
---

## DocumentBuilder.row_format property

Returns an object that represents current table row formatting properties.


```python
@property
def row_format(self) -> aspose.words.tables.RowFormat:
    ...

```

### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# ضبط خيارات تنسيق الجدول لمُنشئ المستند
# سيتم تطبيقها على كل صف وخلية نضيفها به.
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True
builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = aspose.pydrawing.Color.orange
builder.insert_cell()
builder.write('Row 1, Col 1')
builder.insert_cell()
builder.write('Row 1, Col 2')
builder.end_row()
# تغيير التنسيق سيطبقها على الخلية الحالية،
# وأي خلايا جديدة نقوم بإنشائها باستخدام المُنشئ لاحقًا.
# هذا لن يؤثر على الخلايا التي أضفناها مسبقًا.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# زيادة ارتفاع الصف لتناسب النص العمودي.
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 3, Col 1')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 3, Col 2')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTable.docx')
```

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_row()
# أثناء بناء الجدول، سيطبق مُنشئ المستند قيم خصائص RowFormat/CellFormat الحالية.
# على الصف/الخلية الحالية التي يكون المؤشر فيها وأي صفوف/خلايا جديدة يتم إنشاؤها.
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)
builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 2, cell 1.')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 2, cell 2.')
builder.end_row()
builder.end_table()
# الصفوف والخلايا التي أضيفت مسبقًا لا تتأثر بأثر رجعي بالتغييرات في تنسيق المُنشئ.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.BuildTable.docx')
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

* module [aspose.words](../../)
* class [DocumentBuilder](../)

