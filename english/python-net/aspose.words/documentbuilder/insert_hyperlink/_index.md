---
title: DocumentBuilder.insert_hyperlink method
linktitle: insert_hyperlink method
articleTitle: insert_hyperlink method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_hyperlink method. Inserts a hyperlink into the document."
type: docs
weight: 380
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
| display_text | str | Text of the link to be displayed in the document. |
| url_or_bookmark | str | Link destination. Can be a url or a name of a bookmark inside the document. This method always adds apostrophes at the beginning and end of the url. |
| is_bookmark | bool | ``True`` if the previous parameter is a name of a bookmark inside the document; ``False`` is the previous parameter is a URL. |

### Remarks

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
builder = aw.DocumentBuilder(doc=doc)
builder.write('For more information, please visit the ')
# Insert a hyperlink and emphasize it with custom formatting.
# The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
builder.insert_hyperlink('Google website', 'https://www.google.com', False)
builder.font.clear_formatting()
builder.writeln('.')
# Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertHyperlink.docx')
```

Shows how to use a document builder's formatting stack.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Set up font formatting, then write the text that goes before the hyperlink.
builder.font.name = 'Arial'
builder.font.size = 24
builder.write('To visit Google, hold Ctrl and click ')
# Preserve our current formatting configuration on the stack.
builder.push_font()
# Alter the builder's current formatting by applying a new style.
builder.font.style_identifier = aw.StyleIdentifier.HYPERLINK
builder.insert_hyperlink('here', 'http://www.google.com', False)
self.assertEqual(aspose.pydrawing.Color.blue.to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.SINGLE, builder.font.underline)
# Restore the font formatting that we saved earlier and remove the element from the stack.
builder.pop_font()
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), builder.font.color.to_argb())
self.assertEqual(aw.Underline.NONE, builder.font.underline)
builder.write('. We hope you enjoyed the example.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.PushPopFont.docx')
```

Shows how to insert a hyperlink which references a local bookmark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.start_bookmark('Bookmark1')
builder.write('Bookmarked text. ')
builder.end_bookmark('Bookmark1')
builder.writeln('Text outside of the bookmark.')
# Insert a HYPERLINK field that links to the bookmark. We can pass field switches
# to the "insert_hyperlink" method as part of the argument containing the referenced bookmark's name.
builder.font.color = aspose.pydrawing.Color.blue
builder.font.underline = aw.Underline.SINGLE
hyper_link = builder.insert_hyperlink('Link to Bookmark1', 'Bookmark1', True).as_field_hyperlink()
hyper_link.screen_tip = 'Hyperlink Tip'
doc.save(ARTIFACTS_DIR + 'DocumentBuilder.insert_hyperlink_to_local_bookmark.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

