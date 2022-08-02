---
title: contents_font property
second_title: Aspose.Words for Python via .NET API Reference
description: "Font formatting that will be applied to text entered into SDT."
type: docs
weight: 80
url: /python-net/aspose.words.markup/structureddocumenttag/contents_font/
---

## StructuredDocumentTag.contents_font property

Font formatting that will be applied to text entered into **SDT**.



### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()

# Create a structured document tag that will contain plain text.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)

# Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
tag.title = "My plain text"
tag.color = drawing.Color.magenta

# Set a tag for this structured document tag, which is obtainable
# as an XML element named "tag", with the string below in its "@val" attribute.
tag.tag = "MyPlainTextSDT"

# Every structured document tag has a random unique ID.
self.assertGreater(tag.id, 0)

# Set the font for the text inside the structured document tag.
tag.contents_font.name = "Arial"

# Set the font for the text at the end of the structured document tag.
# Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
tag.end_character_font.name = "Arial Black"

# By default, this is False and pressing enter while inside a structured document tag does nothing.
# When set to True, our structured document tag can have multiple lines.

# Set the "multiline" property to "False" to only allow the contents
# of this structured document tag to span a single line.
# Set the "multiline" property to "True" to allow the tag to contain multiple lines of content.
tag.multiline = True

# Set the "Appearance" property to "SdtAppearance.TAGS" to show tags around content.
# By default structured document tag shows as BoundingBox.
tag.appearance = aw.markup.SdtAppearance.TAGS

builder = aw.DocumentBuilder(doc)
builder.insert_node(tag)

# Insert a clone of our structured document tag in a new paragraph.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)

# Use the "remove_self_only" method to remove a structured document tag, while keeping its contents in the document.
tag_clone.remove_self_only()

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.plain_text.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

