---
title: all_caps property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if the font is formatted as all capital letters."
type: docs
weight: 10
url: /python-net/aspose.words/font/all_caps/
---

## Font.all_caps property

True if the font is formatted as all capital letters.


### Examples

Shows how to format a run to display its contents in capitals.

```python
doc = aw.Document()
para = doc.get_child(aw.NodeType.PARAGRAPH, 0, True).as_paragraph()

# There are two ways of getting a run to display its lowercase text in uppercase without changing the contents.
# 1 -  Set the "all_caps" flag to display all characters in regular capitals:
run = aw.Run(doc, "all capitals")
run.font.all_caps = True
para.append_child(run)

para = para.parent_node.append_child(aw.Paragraph(doc)).as_paragraph()

# 2 -  Set the "small_caps" flag to display all characters in small capitals:
# If a character is lower case, it will appear in its upper case form
# but will have the same height as the lower case (the font's x-height).
# Characters that were in upper case originally will look the same.
run = aw.Run(doc, "Small Capitals")
run.font.small_caps = True
para.append_child(run)

doc.save(ARTIFACTS_DIR + "Font.caps.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

