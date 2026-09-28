---
title: DocumentBuilder.insert_cell method
linktitle: insert_cell method
articleTitle: insert_cell method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_cell method. Inserts a table cell into the document."
type: docs
weight: 270
url: /ar/python-net/aspose.words/documentbuilder/insert_cell/
---

## insert_cell() {#default}

Inserts a table cell into the document.


```python
def insert_cell(self):
    ...
```

### Remarks

To start a table, just call [DocumentBuilder.insert_cell()](./#default). After this, any content you add using
other methods of the [DocumentBuilder](../) class will be added to the current cell.

To start a new cell in the same row, call [DocumentBuilder.insert_cell()](./#default) again.

To end a table row call [DocumentBuilder.end_row()](../end_row/#default).

Use the [DocumentBuilder.cell_format](../cell_format/) property to specify cell formatting.




### Returns

The cell node that was just inserted.


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

Shows how to use a document builder to create a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# ابدأ الجدول، ثم املأ الصف الأول بخلتين.
builder.start_table()
builder.insert_cell()
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
# استدعِ طريقة "EndRow" الخاصة بالمُنشئ لبدء صف جديد.
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateTable.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

