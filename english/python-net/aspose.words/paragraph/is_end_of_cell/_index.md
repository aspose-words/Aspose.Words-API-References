---
title: Paragraph.is_end_of_cell property
linktitle: is_end_of_cell property
articleTitle: is_end_of_cell property
second_title: Aspose.Words for Python
description: "Paragraph.is_end_of_cell property. True if this paragraph is the last paragraph in a [Cell](../../../aspose.words.tables/cell/); false otherwise."
type: docs
weight: 50
url: /python-net/aspose.words/paragraph/is_end_of_cell/
---

## Paragraph.is_end_of_cell property

True if this paragraph is the last paragraph in a [Cell](../../../aspose.words.tables/cell/); false otherwise.



### Examples

Shows how to set a table to stay together on the same page.

```python
doc = aw.Document(MY_DIR + "Table spanning two pages.docx")
table = doc.first_section.body.tables[0]

# Enabling keep_with_next for every paragraph in the table except for the
# last ones in the last row will prevent the table from splitting across multiple pages.
for cell in table.get_child_nodes(aw.NodeType.CELL, True):
    cell = cell.as_cell()
    for para in cell.paragraphs:
        para = para.as_paragraph()

        self.assertTrue(para.is_in_cell)

        if not cell.parent_row.is_last_row and para.is_end_of_cell:
            para.paragraph_format.keep_with_next = True

doc.save(ARTIFACTS_DIR + "Table.keep_table_together.docx")
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

