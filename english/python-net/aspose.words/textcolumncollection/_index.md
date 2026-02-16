---
title: TextColumnCollection class
linktitle: TextColumnCollection class
articleTitle: TextColumnCollection class
second_title: Aspose.Words for Python
description: "aspose.words.TextColumnCollection class. A collection of [TextColumn](../textcolumn/) objects that represent all the columns of text in a section of a document"
type: docs
weight: 1320
url: /python-net/aspose.words/textcolumncollection/
---

## TextColumnCollection class

A collection of [TextColumn](../textcolumn/) objects that represent all the columns of text in a section of a document.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/python-net/working-with-sections/) documentation article.




### Remarks

Use [TextColumnCollection.set_count()](./set_count/#int) to set the number of text columns.

To make all columns equal width and spaced evenly, set [TextColumnCollection.evenly_spaced](./evenly_spaced/) to ``True``
and specify the amount of space between the columns in [TextColumnCollection.spacing](./spacing/). MS Word will
automatically calculate column widths.

If you have [TextColumnCollection.evenly_spaced](./evenly_spaced/) set to ``False``, you need to specify width and spacing for each
column individually. Use the indexer to access individual [TextColumn](../textcolumn/) objects.

When using custom column widths, make sure the sum of all column widths and spacings between them
equals page width minus left and right page margins.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a text column at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of columns in the section of a document. |
| [evenly_spaced](./evenly_spaced/) | True if text columns are of equal width and evenly spaced. |
| [line_between](./line_between/) | When ``True``, adds a vertical line between columns. |
| [spacing](./spacing/) | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [width](./width/) | When columns are evenly spaced, gets the width of the columns. |

### Methods

| Name | Description |
| --- | --- |
|[ set_count(new_count)](./set_count/#int) | Arranges text into the specified number of text columns. |

### Examples

Shows how to create multiple evenly spaced columns in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
columns = builder.page_setup.text_columns
columns.spacing = 100
columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ColumnsSameWidth.docx')
```

### See Also

* module [aspose.words](../)
* class [PageSetup](../pagesetup/)
* class [Section](../section/)

