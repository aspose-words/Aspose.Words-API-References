---
title: PreferredWidthType enumeration
linktitle: PreferredWidthType enumeration
articleTitle: PreferredWidthType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.PreferredWidthType enumeration. Specifies the unit of measurement for the preferred width of a table or cell."
type: docs
weight: 80
url: /python-net/aspose.words.tables/preferredwidthtype/
---

## PreferredWidthType enumeration

Specifies the unit of measurement for the preferred width of a table or cell.


### Members

| Name | Description |
| --- | --- |
| AUTO | The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or  will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting. |
| PERCENT | Measure the current item width using a specified percentage. |
| POINTS | Measure the current item width using a specified number of points (1/72 inch). |

### Examples

Shows how to verify the preferred width type and value of a table cell.

```python
doc = aw.Document(MY_DIR + "Tables.docx")

table = doc.first_section.body.tables[0]
first_cell = table.first_row.first_cell

self.assertEqual(aw.tables.PreferredWidthType.PERCENT, first_cell.cell_format.preferred_width.type)
self.assertEqual(11.16, first_cell.cell_format.preferred_width.value)
```

### See Also

* module [aspose.words.tables](../)
* class [PreferredWidth](../preferredwidth/)

