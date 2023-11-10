---
title: PageSetup.characters_per_line property
linktitle: characters_per_line property
articleTitle: characters_per_line property
second_title: Aspose.Words for Python
description: "PageSetup.characters_per_line property. Gets or sets the number of characters per line in the document grid."
type: docs
weight: 100
url: /python-net/aspose.words/pagesetup/characters_per_line/
---

## PageSetup.characters_per_line property

Gets or sets the number of characters per line in the document grid.


```python
@property
def characters_per_line(self) -> int:
    ...

@characters_per_line.setter
def characters_per_line(self, value: int):
    ...

```

### Remarks

Minimum value of the property is 1. Maximum value depends on page width and font size of the Normal
style. Minimum character pitch is 90 percent of the font size. For example, maximum number of characters
per line of a Letter page with one-inch margins is 43.

By default, the property has a value, on which character pitch equals to font size of the Normal
style.




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

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

