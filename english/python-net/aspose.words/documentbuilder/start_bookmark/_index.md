﻿---
title: DocumentBuilder.start_bookmark method
linktitle: start_bookmark method
articleTitle: start_bookmark method
second_title: Aspose.Words for Python
description: "DocumentBuilder.start_bookmark method. Marks the current position in the document as a bookmark start."
type: docs
weight: 650
url: /python-net/aspose.words/documentbuilder/start_bookmark/
---

## start_bookmark(bookmark_name) {#str}

Marks the current position in the document as a bookmark start.


```python
def start_bookmark(self, bookmark_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| bookmark_name | str | Name of the bookmark. |

### Remarks

Bookmarks in a document can overlap and span any range. To create a valid bookmark you need to
call both [DocumentBuilder.start_bookmark()](./#str) and [DocumentBuilder.end_bookmark()](../end_bookmark/#str) with the same *bookmarkName*
parameter.

Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.




### Returns

The bookmark start node that was just created.


### Examples

Shows how create a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# A valid bookmark needs to have document body text enclosed by
# BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
builder.start_bookmark('MyBookmark')
builder.writeln('Hello world!')
builder.end_bookmark('MyBookmark')
self.assertEqual(1, doc.range.bookmarks.count)
self.assertEqual('MyBookmark', doc.range.bookmarks[0].name)
self.assertEqual('Hello world!', doc.range.bookmarks[0].text.strip())
```

Shows how to insert a hyperlink which references a local bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('Bookmark1')
builder.write('Bookmarked text. ')
builder.end_bookmark('Bookmark1')
builder.writeln('Text outside of the bookmark.')
# Insert a HYPERLINK field that links to the bookmark. We can pass field switches
# to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
hyperlink = builder.insert_hyperlink('Link to Bookmark1', 'Bookmark1', True).as_field_hyperlink()
hyperlink.screen_tip = 'Hyperlink Tip'
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlinkToLocalBookmark.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

