---
title: Table.text_wrapping property
linktitle: text_wrapping property
articleTitle: text_wrapping property
second_title: Aspose.Words for Python
description: "Table.text_wrapping property. Gets or sets [Table.text_wrapping](./) for table."
type: docs
weight: 310
url: /de/python-net/aspose.words.tables/table/text_wrapping/
---

## Table.text_wrapping property

Gets or sets [Table.text_wrapping](./) for table.



```python
@property
def text_wrapping(self) -> aspose.words.tables.TextWrapping:
    ...

@text_wrapping.setter
def text_wrapping(self, value: aspose.words.tables.TextWrapping):
    ...

```

### Examples

Shows how to work with table text wrapping.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
builder.font.size = 16
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
# Setzen Sie die Eigenschaft "TextWrapping" auf "TextWrapping.Around", um die Tabelle den Text umfließen zu lassen,
# und schieben Sie sie nach unten in den darunterliegenden Absatz, indem Sie die Position festlegen.
table.text_wrapping = aw.tables.TextWrapping.AROUND
table.absolute_horizontal_distance = 100
table.absolute_vertical_distance = 20
doc.save(file_name=ARTIFACTS_DIR + 'Table.WrapText.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

