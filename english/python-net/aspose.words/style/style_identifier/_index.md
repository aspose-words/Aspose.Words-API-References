---
title: Style.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "Style.style_identifier property. Gets the locale independent style identifier for a built-in style."
type: docs
weight: 160
url: /python-net/aspose.words/style/style_identifier/
---

## Style.style_identifier property

Gets the locale independent style identifier for a built-in style.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

```

### Remarks

For user defined (custom) styles, this property returns [StyleIdentifier.USER](../../styleidentifier/#USER).




### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(MY_DIR + "Table of contents.docx")

# Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if (para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and
        para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9):

        # Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
        tab = para.paragraph_format.tab_stops[0]

        # Replace the first default tab, stop with a custom tab stop.
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(tab.position - 50, tab.alignment, tab.leader)

doc.save(ARTIFACTS_DIR + "Styles.change_tocs_tab_stops.docx")
```

### See Also

* module [aspose.words](../../)
* class [Style](../)
* property [Style.name](../name/)

