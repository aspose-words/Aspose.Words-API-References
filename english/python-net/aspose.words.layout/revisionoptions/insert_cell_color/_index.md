---
title: RevisionOptions.insert_cell_color property
linktitle: insert_cell_color property
articleTitle: insert_cell_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.insert_cell_color property. Allows to specify the color to be used for inserted cells [RevisionType.INSERTION](../../../aspose.words/revisiontype/#INSERTION)"
type: docs
weight: 50
url: /python-net/aspose.words.layout/revisionoptions/insert_cell_color/
---

## RevisionOptions.insert_cell_color property

Allows to specify the color to be used for inserted cells [RevisionType.INSERTION](../../../aspose.words/revisiontype/#INSERTION).
Default value is [RevisionColor.BLUE](../../revisioncolor/#BLUE).



```python
@property
def insert_cell_color(self) -> aspose.words.layout.RevisionColor:
    ...

@insert_cell_color.setter
def insert_cell_color(self, value: aspose.words.layout.RevisionColor):
    ...

```

### Examples

Shows how to work with insert/delete cell revision color.

```python
doc = aw.Document(file_name=MY_DIR + 'Cell revisions.docx')
doc.layout_options.revision_options.insert_cell_color = aw.layout.RevisionColor.LIGHT_BLUE
doc.layout_options.revision_options.delete_cell_color = aw.layout.RevisionColor.DARK_RED
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionCellColor.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

