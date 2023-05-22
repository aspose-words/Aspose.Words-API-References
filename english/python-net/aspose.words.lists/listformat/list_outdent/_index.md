---
title: ListFormat.list_outdent method
linktitle: list_outdent method
articleTitle: list_outdent method
second_title: Aspose.Words for Python
description: "ListFormat.list_outdent method. Decreases the list level of the current paragraph by one level."
type: docs
weight: 80
url: /python-net/aspose.words.lists/listformat/list_outdent/
---

## list_outdent() {#default}

Decreases the list level of the current paragraph by one level.


```python
def list_outdent(self):
    ...
```

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting
for each level specifies what bullet or number is used, left indent, space between
the bullet and text etc.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Aspose.Words main advantages are:")

# A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
# We can create nested lists by increasing the indent level.
# We can begin and end a list by using a document builder's "list_format" property.
# Each paragraph that we add between a list's start and the end will become an item in the list.
# Below are two types of lists that we can create with a document builder.
# 1 -  A bulleted list:
# This list will apply an indent and a bullet symbol ("•") before each paragraph.
builder.list_format.apply_bullet_default()
builder.writeln("Great performance")
builder.writeln("High reliability")
builder.writeln("Quality code and working")
builder.writeln("Wide variety of features")
builder.writeln("Easy to understand API")

# End the bulleted list.
builder.list_format.remove_numbers()

builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln("Aspose.Words allows:")

# 2 -  A numbered list:
# Numbered lists create a logical order for their paragraphs by numbering each item.
builder.list_format.apply_number_default()

# This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
builder.writeln("Opening documents from different formats:")

self.assertEqual(0, builder.list_format.list_level_number)

# Call the "list_indent" method to increase the current list level,
# which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
builder.list_format.list_indent()

self.assertEqual(1, builder.list_format.list_level_number)

# These are the first three list items of the second list level, which will maintain a count
# independent of the count of the first list level. According to the current list format,
# they will have symbols of "a.", "b.", and "c.".
builder.writeln("DOC")
builder.writeln("PDF")
builder.writeln("HTML")

# Call the "list_outdent" method to return to the previous list level.
builder.list_format.list_outdent()

self.assertEqual(0, builder.list_format.list_level_number)

# These two paragraphs will continue the count of the first list level.
# These items will have symbols of "2.", and "3."
builder.writeln("Processing documents")
builder.writeln("Saving documents in different formats:")

# If we increase the list level to a level that we have added items to previously,
# the nested list will be separate from the previous, and its numbering will start from the beginning.
# These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
builder.list_format.list_indent()
builder.writeln("DOC")
builder.writeln("PDF")
builder.writeln("HTML")
builder.writeln("MHTML")
builder.writeln("Plain text")

# Outdent the list level again.
builder.list_format.list_outdent()
builder.writeln("Doing many other things!")

# End the numbered list.
builder.list_format.remove_numbers()

doc.save(ARTIFACTS_DIR + "Lists.apply_default_bullets_and_numbers.docx")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

