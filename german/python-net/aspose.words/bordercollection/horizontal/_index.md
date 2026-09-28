---
title: BorderCollection.horizontal property
linktitle: horizontal property
articleTitle: horizontal property
second_title: Aspose.Words for Python
description: "BorderCollection.horizontal property. Gets the horizontal border that is used between cells or conforming paragraphs."
type: docs
weight: 60
url: /de/python-net/aspose.words/bordercollection/horizontal/
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
# Erstelle einen roten horizontalen Rahmen für den Absatz. Alle anschließend erstellten Absätze erben diese Rahmeneinstellungen.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
borders.horizontal.color = aspose.pydrawing.Color.red
borders.horizontal.line_style = aw.LineStyle.DASH_SMALL_GAP
borders.horizontal.line_width = 3
# Schreibe Text in das Dokument, ohne anschließend einen neuen Absatz zu erstellen.
# Da kein Absatz darunter liegt, wird der horizontale Rahmen nicht sichtbar sein.
builder.write('Paragraph above horizontal border.')
# Sobald wir einen zweiten Absatz hinzufügen, wird der Rahmen des ersten Absatzes sichtbar.
builder.insert_paragraph()
builder.write('Paragraph below horizontal border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.HorizontalBorders.docx')
```

Shows how to apply settings to vertical borders to a table row's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstelle eine Tabelle mit roten und blauen inneren Rahmen.
table = builder.start_table()
i = 0
while i < 3:
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 1')
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 2')
    row = builder.end_row()
    borders = row.row_format.borders
    # Passe das Aussehen der Rahmen an, die zwischen Zeilen erscheinen.
    borders.horizontal.color = aspose.pydrawing.Color.red
    borders.horizontal.line_style = aw.LineStyle.DOT
    borders.horizontal.line_width = 2
    # Passe das Aussehen der Rahmen an, die zwischen Zellen erscheinen.
    borders.vertical.color = aspose.pydrawing.Color.blue
    borders.vertical.line_style = aw.LineStyle.DOT
    borders.vertical.line_width = 2
    i += 1
# Ein Zeilenformat und ein innerer Absatz einer Zelle verwenden unterschiedliche Rahmeneinstellungen.
border = table.first_row.first_cell.last_paragraph.paragraph_format.borders.vertical
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), border.color.to_argb())
self.assertEqual(0, border.line_width)
self.assertEqual(aw.LineStyle.NONE, border.line_style)
doc.save(file_name=ARTIFACTS_DIR + 'Border.VerticalBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

