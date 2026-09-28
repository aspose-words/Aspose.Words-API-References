---
title: Table.clear_shading method
linktitle: clear_shading method
articleTitle: clear_shading method
second_title: Aspose.Words for Python
description: "Table.clear_shading method. Removes all shading on the table."
type: docs
weight: 400
url: /ar/python-net/aspose.words.tables/table/clear_shading/
---

## clear_shading() {#default}

Removes all shading on the table.


```python
def clear_shading(self):
    ...
```

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# حاذِ الجدول إلى مركز الصفحة.
table.alignment = aw.tables.TableAlignment.CENTER
# امسح أي حدود أو تظليل موجود من الجدول.
table.clear_borders()
table.clear_shading()
# أضف حدودًا خضراء إلى مخطط الجدول.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# املأ الخلايا بلون أخضر فاتح صلب.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [Table](../)

