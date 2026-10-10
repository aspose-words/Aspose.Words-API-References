---
title: TextColumn.space_after property
linktitle: space_after property
articleTitle: space_after property
second_title: Aspose.Words for Python
description: "TextColumn.space_after property. Gets or sets the space between this column and the next column in points"
type: docs
weight: 10
url: /fr/python-net/aspose.words/textcolumn/space_after/
---

## TextColumn.space_after property

Gets or sets the space between this column and the next column in points. Not required for the last column.


```python
@property
def space_after(self) -> float:
    ...

@space_after.setter
def space_after(self, value: float):
    ...

```

### Examples

Shows how to create unevenly spaced columns.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
page_setup = builder.page_setup
columns = page_setup.text_columns
columns.evenly_spaced = False
columns.set_count(2)
# Déterminez la quantité d'espace dont nous disposons pour organiser les colonnes.
content_width = page_setup.page_width - page_setup.left_margin - page_setup.right_margin
self.assertAlmostEqual(470.3, content_width, delta=0.01)
# Définissez la première colonne comme étroite.
column = columns[0]
column.width = 100
column.space_after = 20
# Définissez la deuxième colonne pour qu'elle occupe le reste de l'espace disponible à l'intérieur des marges de la page.
column = columns[1]
column.width = content_width - column.width - column.space_after
builder.writeln('Narrow column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Wide column 2.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.CustomColumnWidth.docx')
```

### See Also

* module [aspose.words](../../)
* class [TextColumn](../)

