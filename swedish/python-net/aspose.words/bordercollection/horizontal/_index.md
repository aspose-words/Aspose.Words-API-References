---
title: BorderCollection.horizontal property
linktitle: horizontal property
articleTitle: horizontal property
second_title: Aspose.Words for Python
description: "BorderCollection.horizontal property. Gets the horizontal border that is used between cells or conforming paragraphs."
type: docs
weight: 60
url: /sv/python-net/aspose.words/bordercollection/horizontal/
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
# Skapa en röd horisontell kant för stycket. Alla stycken som skapas efteråt kommer att ärva dessa kantinställningar.
borders = doc.first_section.body.first_paragraph.paragraph_format.borders
borders.horizontal.color = aspose.pydrawing.Color.red
borders.horizontal.line_style = aw.LineStyle.DASH_SMALL_GAP
borders.horizontal.line_width = 3
# Skriv text till dokumentet utan att skapa ett nytt stycke efteråt.
# Eftersom det inte finns något stycke under, kommer den horisontella kanten inte att vara synlig.
builder.write('Paragraph above horizontal border.')
# När vi lägger till ett andra stycke blir kanten på det första stycket synlig.
builder.insert_paragraph()
builder.write('Paragraph below horizontal border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.HorizontalBorders.docx')
```

Shows how to apply settings to vertical borders to a table row's format.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa en tabell med röda och blå inre kanter.
table = builder.start_table()
i = 0
while i < 3:
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 1')
    builder.insert_cell()
    builder.write(f'Row {i + 1}, Column 2')
    row = builder.end_row()
    borders = row.row_format.borders
    # Justera utseendet på kanter som kommer att visas mellan rader.
    borders.horizontal.color = aspose.pydrawing.Color.red
    borders.horizontal.line_style = aw.LineStyle.DOT
    borders.horizontal.line_width = 2
    # Justera utseendet på kanter som kommer att visas mellan celler.
    borders.vertical.color = aspose.pydrawing.Color.blue
    borders.vertical.line_style = aw.LineStyle.DOT
    borders.vertical.line_width = 2
    i += 1
# Ett radformat och ett cells inre stycke använder olika kantinställningar.
border = table.first_row.first_cell.last_paragraph.paragraph_format.borders.vertical
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), border.color.to_argb())
self.assertEqual(0, border.line_width)
self.assertEqual(aw.LineStyle.NONE, border.line_style)
doc.save(file_name=ARTIFACTS_DIR + 'Border.VerticalBorders.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

