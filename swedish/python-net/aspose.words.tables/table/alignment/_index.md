---
title: Table.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "Table.alignment property. Specifies how an inline table is aligned in the document."
type: docs
weight: 40
url: /sv/python-net/aspose.words.tables/table/alignment/
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
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Justera tabellen till mitten av sidan.
table.alignment = aw.tables.TableAlignment.CENTER
# Rensa eventuella befintliga kanter och skuggning från tabellen.
table.clear_borders()
table.clear_shading()
# Lägg till gröna kanter runt tabellens kontur.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# Fyll cellerna med en ljusgrön solid färg.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

