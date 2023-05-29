---
title: FindReplaceOptions.smart_paragraph_break_replacement property
linktitle: smart_paragraph_break_replacement property
articleTitle: smart_paragraph_break_replacement property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.smart_paragraph_break_replacement property. Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph."
type: docs
weight: 160
url: /python-net/aspose.words.replacing/findreplaceoptions/smart_paragraph_break_replacement/
---

## FindReplaceOptions.smart_paragraph_break_replacement property

Gets or sets a boolean value indicating either it is allowed to replace paragraph break
when there is no next sibling paragraph.

The default value is ``False``.



This option allows to replace paragraph break when there is no next sibling paragraph to which all child
nodes can be moved, by finding any (not necessarily sibling) next paragraph after the paragraph being replaced.


### Examples

Shows how to remove paragraph from a table cell with a nested table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create table with paragraph and inner table in first cell.
builder.start_table()
builder.insert_cell()
builder.write("TEXT1")
builder.start_table()
builder.insert_cell()
builder.end_table()
builder.end_table()
builder.writeln()

options = aw.replacing.FindReplaceOptions()
# When the following option is set to 'True', Aspose.Words will remove paragraph's text
# completely with its paragraph mark. Otherwise, Aspose.Words will mimic Word and remove
# only paragraph's text and leaves the paragraph mark intact (when a table follows the text).
options.smart_paragraph_break_replacement = is_smart_paragraph_break_replacement
doc.range.replace("TEXT1&p", "", options)

doc.save(ARTIFACTS_DIR + "Table.remove_paragraph_text_and_mark.docx")
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

