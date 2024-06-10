---
title: ParagraphFormat.keep_with_next property
linktitle: keep_with_next property
articleTitle: keep_with_next property
second_title: Aspose.Words for Python
description: "ParagraphFormat.keep_with_next property. True if the paragraph is to remains on the same page as the paragraph that follows it."
type: docs
weight: 170
url: /python-net/aspose.words/paragraphformat/keep_with_next/
---

## ParagraphFormat.keep_with_next property

True if the paragraph is to remains on the same page as the paragraph that follows it.


```python
@property
def keep_with_next(self) -> bool:
    ...

@keep_with_next.setter
def keep_with_next(self, value: bool):
    ...

```

### Examples

Shows how to set a table to stay together on the same page.

```python
doc = aw.Document(file_name=MY_DIR + 'Table spanning two pages.docx')
table = doc.first_section.body.tables[0]
# Enabling KeepWithNext for every paragraph in the table except for the
# last ones in the last row will prevent the table from splitting across multiple pages.
for cell in table.get_child_nodes(aw.NodeType.CELL, True):
    cell = cell.as_cell()
    for para in cell.paragraphs:
        para = para.as_paragraph()
        self.assertTrue(para.is_in_cell)
        if not (cell.parent_row.is_last_row and para.is_end_of_cell):
            para.paragraph_format.keep_with_next = True
doc.save(file_name=ARTIFACTS_DIR + 'Table.KeepTableTogether.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

