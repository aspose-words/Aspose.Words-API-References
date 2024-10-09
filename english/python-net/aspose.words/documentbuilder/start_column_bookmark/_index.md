---
title: DocumentBuilder.start_column_bookmark method
linktitle: start_column_bookmark method
articleTitle: start_column_bookmark method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_column_bookmark method. Marks the current position in the document as a column bookmark start"
type: docs
weight: 660
url: /python-net/aspose.words/documentbuilder/start_column_bookmark/
---

## start_column_bookmark(bookmark_name) {#str}

Marks the current position in the document as a column bookmark start. The position must be in a table cell.


```python
def start_column_bookmark(self, bookmark_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | Name of the bookmark. |

### Remarks

A column bookmark covers one or more columns in a range of rows. To create a valid bookmark you
need to call both [DocumentBuilder.start_column_bookmark()](./#str) and [DocumentBuilder.end_column_bookmark()](../end_column_bookmark/#str) with the same
*bookmarkName* parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.

The actual position of the inserted [BookmarkStart](../../bookmarkstart/) node may differ from the current document
builder position.




### Returns

The bookmark start node that was just created.


### Examples

Shows how to create a column bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.start_table()
builder.insert_cell()
# Cells 1,2,4,5 will be bookmarked.
builder.start_column_bookmark('MyBookmark_1')
# Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
builder.start_column_bookmark('MyBookmark_1')
builder.start_column_bookmark('BadStartBookmark')
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.insert_cell()
builder.write('Cell 3')
builder.end_row()
builder.insert_cell()
builder.write('Cell 4')
builder.insert_cell()
builder.write('Cell 5')
builder.end_column_bookmark('MyBookmark_1')
builder.end_column_bookmark('MyBookmark_1')
builder.insert_cell()
builder.write('Cell 6')
builder.end_row()
builder.end_table()
doc.save(ARTIFACTS_DIR + 'Bookmarks.create_column_bookmark.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

