---
title: DocumentBuilder.paragraph_format property
linktitle: paragraph_format property
articleTitle: paragraph_format property
second_title: Aspose.Words for Python
description: "DocumentBuilder.paragraph_format property. Returns an object that represents current paragraph formatting properties."
type: docs
weight: 170
url: /de/python-net/aspose.words/documentbuilder/paragraph_format/
---

## DocumentBuilder.paragraph_format property

Returns an object that represents current paragraph formatting properties.


```python
@property
def paragraph_format(self) -> aspose.words.ParagraphFormat:
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
# Lege einige Formatierungsoptionen für Text- und Tabellenanzeige fest.
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.from_argb(198, 217, 241)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = 'Arial'
builder.font.bold = True
# Das Konfigurieren der Formatierungsoptionen in einem Dokument-Builder wendet sie an
# auf die aktuelle Zelle/Zeile, in der sich sein Cursor befindet,
# sowie auf alle neuen Zellen und Zeilen, die mit diesem Builder erstellt werden.
builder.write('Header Row,\n Cell 1')
builder.insert_cell()
builder.write('Header Row,\n Cell 2')
builder.insert_cell()
builder.write('Header Row,\n Cell 3')
builder.end_row()
# Konfiguriere die Formatierungsobjekte des Builders neu für neue Zeilen und Zellen, die wir gleich erstellen werden.
# Der Builder wird diese nicht auf die bereits erstellte erste Zeile anwenden, damit sie als Kopfzeile hervorsticht.
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

* module [aspose.words](../../)
* class [DocumentBuilder](../)

