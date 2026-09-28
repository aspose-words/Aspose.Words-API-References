---
title: BorderCollection.horizontal property
linktitle: horizontal property
articleTitle: horizontal property
second_title: Aspose.Words for Python
description: "BorderCollection.horizontal property. Gets the horizontal border that is used between cells or conforming paragraphs."
type: docs
weight: 60
url: /ar/python-net/aspose.words/bordercollection/horizontal/
---

## BorderCollection.horizontal property

Gets the horizontal border that is used between cells or conforming paragraphs.


```python
@property
def horizontal(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply settings to horizontal borders to a paragraph's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إنشاء حد أفقي أحمر للفقرة. أي فقرات تُنشأ لاحقًا ستورث إعدادات هذا الحد.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
borders.horizontal.color = aspose.pydrawing.Color.red
borders.horizontal.line_style = aw.LineStyle.DASH_SMALL_GAP
borders.horizontal.line_width = 3
# اكتب نصًا إلى المستند دون إنشاء فقرة جديدة بعد ذلك.
# نظرًا لعدم وجود فقرة تحته، لن يكون الحد الأفقي مرئيًا.
builder.write('Paragraph above horizontal border.')
# بمجرد إضافة فقرة ثانية، سيصبح حد الفقرة الأولى مرئيًا.
builder.insert_paragraph()
builder.write('Paragraph below horizontal border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.HorizontalBorders.docx')
```

Shows how to apply settings to vertical borders to a table row's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إنشاء جدول بحدود داخلية حمراء وزرقاء.
table = builder.start_table()
i = 0
while i < 3:
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 1')
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 2')
    row = builder.end_row()
    borders = row.row_format.borders
    # ضبط مظهر الحدود التي ستظهر بين الصفوف.
    borders.horizontal.color = aspose.pydrawing.Color.red
    borders.horizontal.line_style = aw.LineStyle.DOT
    borders.horizontal.line_width = 2
    # ضبط مظهر الحدود التي ستظهر بين الخلايا.
    borders.vertical.color = aspose.pydrawing.Color.blue
    borders.vertical.line_style = aw.LineStyle.DOT
    borders.vertical.line_width = 2
    i += 1
# تنسيق الصف والفقرة الداخلية للخلية يستخدمان إعدادات حدود مختلفة.
border = table.first_row.first_cell.last_paragraph.paragraph_format.borders.vertical
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), border.color.to_argb())
self.assertEqual(0, border.line_width)
self.assertEqual(aw.LineStyle.NONE, border.line_style)
doc.save(file_name=ARTIFACTS_DIR + 'Border.VerticalBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

