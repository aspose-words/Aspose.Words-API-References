---
title: ControlChar.SPACE_CHAR property
linktitle: SPACE_CHAR property
articleTitle: SPACE_CHAR property
second_title: Aspose.Words for Python
description: "ControlChar.SPACE_CHAR property. Space character: (char)32."
type: docs
weight: 260
url: /python-net/aspose.words/controlchar/SPACE_CHAR/
---

## ControlChar.SPACE_CHAR property

Space character: (char)32.


```python
@property
def SPACE_CHAR(self) -> str:
    ...

```

### Examples

Shows how to add various control characters to a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add a regular space.
builder.write("Before space." + aw.ControlChar.SPACE_CHAR + "After space.")

# Add an NBSP, which is a non-breaking space.
# Unlike the regular space, this space cannot have an automatic line break at its position.
builder.write("Before space." + aw.ControlChar.NON_BREAKING_SPACE + "After space.")

# Add a tab character.
builder.write("Before tab." + aw.ControlChar.TAB + "After tab.")

# Add a line break.
builder.write("Before line break." + aw.ControlChar.LINE_BREAK + "After line break.")

# Add a new line and starts a new paragraph.
self.assertEqual(1, doc.first_section.body.get_child_nodes(aw.NodeType.PARAGRAPH, True).count)
builder.write("Before line feed." + aw.ControlChar.LINE_FEED + "After line feed.")
self.assertEqual(2, doc.first_section.body.get_child_nodes(aw.NodeType.PARAGRAPH, True).count)

# The line feed character has two versions.
self.assertEqual(aw.ControlChar.LINE_FEED, aw.ControlChar.LF)

# Carriage returns and line feeds can be represented together by one character.
self.assertEqual(aw.ControlChar.CR_LF, aw.ControlChar.CR + aw.ControlChar.LF)

# Add a paragraph break, which will start a new paragraph.
builder.write("Before paragraph break." + aw.ControlChar.PARAGRAPH_BREAK + "After paragraph break.")
self.assertEqual(3, doc.first_section.body.get_child_nodes(aw.NodeType.PARAGRAPH, True).count)

# Add a section break. This does not make a new section or paragraph.
self.assertEqual(1, doc.sections.count)
builder.write("Before section break." + aw.ControlChar.SECTION_BREAK + "After section break.")
self.assertEqual(1, doc.sections.count)

# Add a page break.
builder.write("Before page break." + aw.ControlChar.PAGE_BREAK + "After page break.")

# A page break is the same value as a section break.
self.assertEqual(aw.ControlChar.PAGE_BREAK, aw.ControlChar.SECTION_BREAK)

# Insert a new section, and then set its column count to two.
doc.append_child(aw.Section(doc))
builder.move_to_section(1)
builder.current_section.page_setup.text_columns.set_count(2)

# We can use a control character to mark the point where text moves to the next column.
builder.write("Text at end of column 1." + aw.ControlChar.COLUMN_BREAK + "Text at beginning of column 2.")

doc.save(ARTIFACTS_DIR + "ControlChar.insert_control_chars.docx")

# There are char and string counterparts for most characters.
self.assertEqual(aw.ControlChar.CELL, aw.ControlChar.CELL_CHAR)
self.assertEqual(aw.ControlChar.NON_BREAKING_SPACE, aw.ControlChar.NON_BREAKING_SPACE_CHAR)
self.assertEqual(aw.ControlChar.TAB, aw.ControlChar.TAB_CHAR)
self.assertEqual(aw.ControlChar.LINE_BREAK, aw.ControlChar.LINE_BREAK_CHAR)
self.assertEqual(aw.ControlChar.LINE_FEED, aw.ControlChar.LINE_FEED_CHAR)
self.assertEqual(aw.ControlChar.PARAGRAPH_BREAK, aw.ControlChar.PARAGRAPH_BREAK_CHAR)
self.assertEqual(aw.ControlChar.SECTION_BREAK, aw.ControlChar.SECTION_BREAK_CHAR)
self.assertEqual(aw.ControlChar.PAGE_BREAK, aw.ControlChar.SECTION_BREAK_CHAR)
self.assertEqual(aw.ControlChar.COLUMN_BREAK, aw.ControlChar.COLUMN_BREAK_CHAR)
```

### See Also

* module [aspose.words](../../)
* class [ControlChar](../)

