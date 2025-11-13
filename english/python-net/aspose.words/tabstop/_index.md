---
title: TabStop class
linktitle: TabStop class
articleTitle: TabStop class
second_title: Aspose.Words for Python
description: "aspose.words.TabStop class. Represents a single custom tab stop"
type: docs
weight: 1270
url: /python-net/aspose.words/tabstop/
---

## TabStop class

Represents a single custom tab stop. The [TabStop](./) object is a member of the
[TabStopCollection](../tabstopcollection/) collection.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

Normally, a tab stop specifies a position where a tab stop exists. But because
tab stops can be inherited from parent styles, it might be needed for the child object
to define explicitly that there is no tab stop at a given position. To clear
an inherited tab stop at a given position, create a [TabStop](./) object and set
[TabStop.alignment](./alignment/) to [TabAlignment.CLEAR](../tabalignment/#CLEAR).

For more information see [TabStopCollection](../tabstopcollection/).




### Constructors
| Name | Description |
| --- | --- |
| [TabStop(position)](./__init__/#float) | Initializes a new instance of this class. |
| [TabStop(position, alignment, leader)](./__init__/#float_tabalignment_tableader) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [alignment](./alignment/) | Gets or sets the alignment of text at this tab stop. |
| [is_clear](./is_clear/) | Returns ``True`` if this tab stop clears any existing tab stops in this position. |
| [leader](./leader/) | Gets or sets the type of the leader line displayed under the tab character. |
| [position](./position/) | Gets the position of the tab stop in points. |

### Methods

| Name | Description |
| --- | --- |
|[ equals(rhs)](./equals/#tabstop) | Compares with the specified [TabStop](./). |

### Examples

Shows how to modify the position of the right tab stop in TOC related paragraphs.

```python
doc = aw.Document(file_name=MY_DIR + 'Table of contents.docx')
# Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    if para.paragraph_format.style.style_identifier >= aw.StyleIdentifier.TOC1 and para.paragraph_format.style.style_identifier <= aw.StyleIdentifier.TOC9:
        # Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
        tab = para.paragraph_format.tab_stops[0]
        # Replace the first default tab, stop with a custom tab stop.
        para.paragraph_format.tab_stops.remove_by_position(tab.position)
        para.paragraph_format.tab_stops.add(position=tab.position - 50, alignment=tab.alignment, leader=tab.leader)
doc.save(file_name=ARTIFACTS_DIR + 'Styles.ChangeTocsTabStops.docx')
```

### See Also

* module [aspose.words](../)
* class [ParagraphFormat](../paragraphformat/)
* class [TabStopCollection](../tabstopcollection/)
* property [Document.default_tab_stop](../document/default_tab_stop/)

