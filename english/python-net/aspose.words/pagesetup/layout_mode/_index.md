---
title: PageSetup.layout_mode property
linktitle: layout_mode property
articleTitle: layout_mode property
second_title: Aspose.Words for Python
description: "PageSetup.layout_mode property. Gets or sets the layout mode of this section."
type: docs
weight: 190
url: /python-net/aspose.words/pagesetup/layout_mode/
---

## PageSetup.layout_mode property

Gets or sets the layout mode of this section.


### Examples

Shows how to specify a for the number of characters that each line may have.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Enable pitching, and then use it to set the number of characters per line in this section.
builder.page_setup.layout_mode = aw.SectionLayoutMode.GRID
builder.page_setup.characters_per_line = 10

# The number of characters also depends on the size of the font.
doc.styles.get_by_name("Normal").font.size = 20

self.assertEqual(8, doc.first_section.page_setup.characters_per_line)

builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

doc.save(ARTIFACTS_DIR + "PageSetup.characters_per_line.docx")
```

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
* class [PageSetup](../)

