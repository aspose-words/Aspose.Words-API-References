---
title: PreferredWidth.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "PreferredWidth.equals method. Determines whether the specified [PreferredWidth](../) is equal in value to the current [PreferredWidth](../)."
type: docs
weight: 40
url: /sv/python-net/aspose.words.tables/preferredwidth/equals/
---

## equals(other) {#preferredwidth}

Determines whether the specified [PreferredWidth](../) is equal in value to the current [PreferredWidth](../).



```python
def equals(self, other: aspose.words.tables.PreferredWidth):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| other | [PreferredWidth](../) |  |

### Examples

Shows how to set a preferred width for table cells.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# Det finns två sätt att tillämpa klassen "PreferredWidth" på tabellceller.
# 1 -  Ställ in en absolut föredragen bredd baserad på punkter:
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_points(40)
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_yellow
builder.writeln(f'Cell with a width of {builder.cell_format.preferred_width}.')
# 2 -  Ställ in en relativ föredragen bredd baserad på procent av tabellens bredd:
builder.insert_cell()
builder.cell_format.preferred_width = aw.tables.PreferredWidth.from_percent(20)
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_blue
builder.writeln(f'Cell with a width of {builder.cell_format.preferred_width}.')
builder.insert_cell()
# En cell utan angiven föredragen bredd kommer att ta upp resten av det tillgängliga utrymmet.
builder.cell_format.preferred_width = aw.tables.PreferredWidth.AUTO
# Varje konfiguration av egenskapen "PreferredWidth" skapar ett nytt objekt.
self.assertNotEqual(hash(table.first_row.cells[1].cell_format.preferred_width), hash(builder.cell_format.preferred_width))
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_green
builder.writeln('Automatically sized cell.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertCellsWithPreferredWidths.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [PreferredWidth](../)

