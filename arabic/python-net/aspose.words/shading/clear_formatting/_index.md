---
title: Shading.clear_formatting method
linktitle: clear_formatting method
articleTitle: clear_formatting method
second_title: Aspose.Words for Python
description: "Shading.clear_formatting method. Removes shading from the object."
type: docs
weight: 80
url: /ar/python-net/aspose.words/shading/clear_formatting/
---

## clear_formatting() {#default}

Removes shading from the object.


```python
def clear_formatting(self):
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

### See Also

* module [aspose.words](../../)
* class [Shading](../)

