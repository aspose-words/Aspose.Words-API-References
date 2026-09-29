---
title: TextColumnCollection.evenly_spaced property
linktitle: evenly_spaced property
articleTitle: evenly_spaced property
second_title: Aspose.Words for Python
description: "TextColumnCollection.evenly_spaced property. True if text columns are of equal width and evenly spaced."
type: docs
weight: 30
url: /sv/python-net/aspose.words/textcolumncollection/evenly_spaced/
---

## TextColumnCollection.evenly_spaced property

True if text columns are of equal width and evenly spaced.


```python
@property
def evenly_spaced(self) -> bool:
    ...

@evenly_spaced.setter
def evenly_spaced(self, value: bool):
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
# Bestäm hur mycket utrymme vi har tillgängligt för att ordna kolumner.
content_width = page_setup.page_width - page_setup.left_margin - page_setup.right_margin
self.assertAlmostEqual(470.3, content_width, delta=0.01)
# Ställ in den första kolumnen så att den är smal.
column = columns[0]
column.width = 100
column.space_after = 20
# Ställ in den andra kolumnen så att den tar resten av det tillgängliga utrymmet inom sidans marginaler.
column = columns[1]
column.width = content_width - column.width - column.space_after
builder.writeln('Narrow column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Wide column 2.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.CustomColumnWidth.docx')
```

### See Also

* module [aspose.words](../../)
* class [TextColumnCollection](../)

