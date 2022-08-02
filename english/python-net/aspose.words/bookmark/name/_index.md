---
title: name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the name of the bookmark."
type: docs
weight: 60
url: /python-net/aspose.words/bookmark/name/
---

## Bookmark.name property

Gets or sets the name of the bookmark.

Note that if you change the name of a bookmark to a name that already exists in the document,
no error will be given and only the first bookmark will be stored when you save the document.


### Examples

Shows how to insert a bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# A valid bookmark has a name, a BookmarkStart, and a BookmarkEnd node.
# Any whitespace in the names of bookmarks will be converted to underscores if we open the saved document with Microsoft Word.
# If we highlight the bookmark's name in Microsoft Word via Insert -> Links -> Bookmark, and press "Go To",
# the cursor will jump to the text enclosed between the BookmarkStart and BookmarkEnd nodes.
builder.start_bookmark("My Bookmark")
builder.write("Contents of MyBookmark.")
builder.end_bookmark("My Bookmark")

# Bookmarks are stored in this collection.
self.assertEqual("My Bookmark", doc.range.bookmarks[0].name)

doc.save(ARTIFACTS_DIR + "Bookmarks.insert.docx")
```

### See Also

* module [aspose.words](../../)
* class [Bookmark](../)

