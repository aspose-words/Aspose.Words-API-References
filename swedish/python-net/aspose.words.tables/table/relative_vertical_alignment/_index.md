---
title: Table.relative_vertical_alignment property
linktitle: relative_vertical_alignment property
articleTitle: relative_vertical_alignment property
second_title: Aspose.Words for Python
description: "Table.relative_vertical_alignment property. Gets or sets floating table relative vertical alignment."
type: docs
weight: 240
url: /sv/python-net/aspose.words.tables/table/relative_vertical_alignment/
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
# Ställ in tabellens placering till en plats på sidan, till exempel i det här fallet, det nedre högra hörnet.
table.relative_vertical_alignment = aw.drawing.VerticalAlignment.BOTTOM
table.relative_horizontal_alignment = aw.drawing.HorizontalAlignment.RIGHT
table = builder.start_table()
builder.insert_cell()
builder.write('Table 2, cell 1')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
# Vi kan också ange ett horisontellt och vertikalt avstånd i punkter från styckets placering där vi infogade tabellen.
table.absolute_vertical_distance = 50
table.absolute_horizontal_distance = 100
doc.save(file_name=ARTIFACTS_DIR + 'Table.ChangeFloatingTableProperties.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

