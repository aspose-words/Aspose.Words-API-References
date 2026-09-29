---
title: Table.relative_vertical_alignment property
linktitle: relative_vertical_alignment property
articleTitle: relative_vertical_alignment property
second_title: Aspose.Words for Python
description: "Table.relative_vertical_alignment property. Gets or sets floating table relative vertical alignment."
type: docs
weight: 240
url: /it/python-net/aspose.words.tables/table/relative_vertical_alignment/
---

## Table.relative_vertical_alignment property

Gets or sets floating table relative vertical alignment.


```python
@property
def relative_vertical_alignment(self) -> aspose.words.drawing.VerticalAlignment:
    ...

@relative_vertical_alignment.setter
def relative_vertical_alignment(self, value: aspose.words.drawing.VerticalAlignment):
    ...

```

### Examples

Shows how set the location of floating tables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Table 1, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Imposta la posizione della tabella in un punto della pagina, ad esempio, in questo caso, nell'angolo in basso a destra.
table.relative_vertical_alignment = aw.drawing.VerticalAlignment.BOTTOM
table.relative_horizontal_alignment = aw.drawing.HorizontalAlignment.RIGHT
table = builder.start_table()
builder.insert_cell()
builder.write('Table 2, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Possiamo anche impostare un offset orizzontale e verticale in punti rispetto alla posizione del paragrafo in cui abbiamo inserito la tabella.
table.absolute_vertical_distance = 50
table.absolute_horizontal_distance = 100
doc.save(file_name=ARTIFACTS_DIR + 'Table.ChangeFloatingTableProperties.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

