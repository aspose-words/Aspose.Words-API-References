---
title: BorderCollection.right property
linktitle: right property
articleTitle: right property
second_title: Aspose.Words for Python
description: "BorderCollection.right property. Gets the right border."
type: docs
weight: 100
url: /de/python-net/aspose.words/bordercollection/right/
---

## BorderCollection.right property

Gets the right border.


```python
@property
def right(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Starten Sie eine Tabelle und legen Sie eine Standardfarbe/-stärke für ihre Rahmen fest.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2, aspose.pydrawing.Color.black)
# Erstellen Sie eine Zeile mit zwei Zellen mit unterschiedlichen Hintergrundfarben.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_sky_blue
builder.writeln('Row 1, Cell 1.')
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
builder.writeln('Row 1, Cell 2.')
builder.end_row()
# Setzen Sie die Zellenformatierung zurück, um die Hintergrundfarben zu deaktivieren
# Legen Sie eine benutzerdefinierte Rahmenstärke für alle neuen vom Builder erstellten Zellen fest,
# und bauen Sie dann eine zweite Zeile.
builder.cell_format.clear_formatting()
builder.cell_format.borders.left.line_width = 4
builder.cell_format.borders.right.line_width = 4
builder.cell_format.borders.top.line_width = 4
builder.cell_format.borders.bottom.line_width = 4
builder.insert_cell()
builder.writeln('Row 2, Cell 1.')
builder.insert_cell()
builder.writeln('Row 2, Cell 2.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.TableBordersAndShading.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

