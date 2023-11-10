---
title: Table.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "Table.alignment property. Specifies how an inline table is aligned in the document."
type: docs
weight: 40
url: /python-net/aspose.words.tables/table/alignment/
---

## Table.alignment property

Specifies how an inline table is aligned in the document.


```python
@property
def alignment(self) -> aspose.words.tables.TableAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.tables.TableAlignment):
    ...

```

### Remarks

The default value is [TableAlignment.LEFT](../../tablealignment/#LEFT).




### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(MY_DIR + "Tables.docx")
table = doc.first_section.body.tables[0]

# Align the table to the center of the page.
table.alignment = aw.tables.TableAlignment.CENTER

# Clear any existing borders and shading from the table.
table.clear_borders()
table.clear_shading()

# Add green borders to the outline of the table.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, drawing.Color.green, True)

# Fill the cells with a light green solid color.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, drawing.Color.light_green, drawing.Color.empty())

doc.save(ARTIFACTS_DIR + "Table.set_outline_borders.docx")
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

