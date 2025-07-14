---
title: Row.hidden property
linktitle: hidden property
articleTitle: hidden property
second_title: Aspose.Words for Python
description: "Row.hidden property. Gets or sets a flag indicating whether this row is hidden or not."
type: docs
weight: 40
url: /python-net/aspose.words.tables/row/hidden/
---

## Row.hidden property

Gets or sets a flag indicating whether this row is hidden or not.


```python
@property
def hidden(self) -> bool:
    ...

@hidden.setter
def hidden(self, value: bool):
    ...

```

### Remarks

Hidden row is not supported for WordML and ODT documents.


### Examples

Shows how to hide a table row.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
row = doc.first_section.body.tables[0].first_row
row.hidden = True
doc.save(file_name=ARTIFACTS_DIR + 'Table.HiddenRow.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Table.HiddenRow.docx')
row = doc.first_section.body.tables[0].first_row
self.assertTrue(row.hidden)
for cell in row.cells:
    cell = cell.as_cell()
    for para in cell.paragraphs:
        para = para.as_paragraph()
        for run in para.runs:
            run = run.as_run()
            self.assertTrue(run.font.hidden)
```

### See Also

* module [aspose.words.tables](../../)
* class [Row](../)

