---
title: snap_to_grid property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph."
type: docs
weight: 280
url: /python-net/aspose.words/paragraphformat/snap_to_grid/
---

## ParagraphFormat.snap_to_grid property

Specifies whether the current paragraph should use the document grid lines per page settings
when laying out the contents in the paragraph.


### Examples

Shows how to specify a limit for the number of lines that each page may have.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Enable pitching, and then use it to set the number of lines per page in this section.
# A large enough font size will push some lines down onto the next page to avoid overlapping characters.
builder.page_setup.layout_mode = aw.SectionLayoutMode.LINE_GRID
builder.page_setup.lines_per_page = 15

builder.paragraph_format.snap_to_grid = True

for i in range(30):
    builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ")

doc.save(ARTIFACTS_DIR + "PageSetup.lines_per_page.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

