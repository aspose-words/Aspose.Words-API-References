---
title: ListLevel.remove_tab_stop method
linktitle: remove_tab_stop method
articleTitle: remove_tab_stop method
second_title: Aspose.Words for Python
description: "ListLevel.remove_tab_stop method. Removes tab stop from the list level."
type: docs
weight: 190
url: /python-net/aspose.words.lists/listlevel/remove_tab_stop/
---

## remove_tab_stop() {#default}

Removes tab stop from the list level.


```python
def remove_tab_stop(self):
    ...
```

### Examples

Shows how to clear the list level tab stop.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Create a list with default formatting.
builder.list_format.apply_number_default()
builder.writeln("Numbered list item 1")
builder.writeln("Numbered list item 2")
# Get the list level and remove its tab stop.
list_level = builder.list_format.list_level
list_level.remove_tab_stop()
doc.save(file_name=ARTIFACTS_DIR + "Paragraph.RemoveTabStopFromListLevel.docx")
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

