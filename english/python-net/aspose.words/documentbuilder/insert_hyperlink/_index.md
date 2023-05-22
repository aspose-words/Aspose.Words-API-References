---
title: DocumentBuilder.insert_hyperlink method
linktitle: insert_hyperlink method
articleTitle: insert_hyperlink method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_hyperlink method. Inserts a hyperlink into the document."
type: docs
weight: 360
url: /python-net/aspose.words/documentbuilder/insert_hyperlink/
---

## insert_hyperlink(display_text, url_or_bookmark, is_bookmark) {#str_str_bool}

Inserts a hyperlink into the document.


```python
def insert_hyperlink(self, display_text: str, url_or_bookmark: str, is_bookmark: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| display_text | str |  |
| url_or_bookmark | str |  |
| is_bookmark | bool |  |

Note that you need to specify font formatting for the hyperlink display text explicitly
using the [DocumentBuilder.font](../font/) property.

This methods internally calls [DocumentBuilder.insert_field()](../insert_field/#str) to insert an MS Word HYPERLINK field
into the document.




### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.


### Examples

Shows how to insert a hyperlink field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("For more information, please visit the ")

# Insert a hyperlink and emphasize it with custom formatting.
# The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = drawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink("Google website", "https://www.google.com", False)
builder.font.clear_formatting()
builder.writeln(".")

# Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_hyperlink.docx")
```

Shows how to use a document builder's formatting stack.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set up font formatting, then write the text that goes before the hyperlink.
builder.font.name = "Arial"
builder.font.size = 24
builder.write("To visit Google, hold Ctrl and click ")

# Preserve our current formatting configuration on the stack.
builder.push_font()

# Alter the builder's current formatting by applying a new style.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink("here", "http://www.google.com", False)

self.assertEqual(drawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)

# Restore the font formatting that we saved earlier and remove the element from the stack.
builder.pop_font()

self.assertEqual(drawing.Color.empty().to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.NONE, builder.font.underline)

builder.write(". We hope you enjoyed the example.")

doc.save(ARTIFACTS_DIR + "DocumentBuilder.push_pop_font.docx")
```

Shows how to insert a hyperlink which references a local bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.start_bookmark("Bookmark1")
builder.write("Bookmarked text. ")
builder.end_bookmark("Bookmark1")
builder.writeln("Text outside of the bookmark.")

# Insert a HYPERLINK field that links to the bookmark. We can pass field switches
# to the "insert_hyperlink" method as part of the argument containing the referenced bookmark's name.
builder.font.color = drawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink("Link to Bookmark1", "Bookmark1\" \\o \"Hyperlink Tip", True)

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_hyperlink_to_local_bookmark.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

