---
title: RevisionOptions.delete_cell_color property
linktitle: delete_cell_color property
articleTitle: delete_cell_color property
second_title: Aspose.Words for Python
description: "RevisionOptions.delete_cell_color property. Allows to specify the color to be used for deleted cells [RevisionType.DELETION](../../../aspose.words/revisiontype/#DELETION)"
type: docs
weight: 20
url: /python-net/aspose.words.layout/revisionoptions/delete_cell_color/
---

## RevisionOptions.delete_cell_color property

Allows to specify the color to be used for deleted cells [RevisionType.DELETION](../../../aspose.words/revisiontype/#DELETION).
Default value is [RevisionColor.PINK](../../revisioncolor/#PINK).



```python
@property
def delete_cell_color(self) -> aspose.words.layout.RevisionColor:
    ...

@delete_cell_color.setter
def delete_cell_color(self, value: aspose.words.layout.RevisionColor):
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

