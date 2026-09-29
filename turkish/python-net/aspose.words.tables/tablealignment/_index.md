---
title: TableAlignment enumeration
linktitle: TableAlignment enumeration
articleTitle: TableAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.TableAlignment enumeration. Specifies alignment for an inline table."
type: docs
weight: 130
url: /tr/python-net/aspose.words.tables/tablealignment/
---

## TableAlignment enumeration

Specifies alignment for an inline table.


### Members

| Name | Description |
| --- | --- |
| LEFT | The table is aligned to the left. |
| CENTER | The table is centered. |
| RIGHT | The table is aligned to the right. |

### Examples

Shows how to apply an outline border to a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Tables.docx')
table = doc.first_section.body.tables[0]
# Tabloyu sayfanın ortasına hizalayın.
table.alignment = aw.tables.TableAlignment.CENTER
# Tablodaki mevcut kenarlıkları ve gölgelendirmeyi temizleyin.
table.clear_borders()
table.clear_shading()
# Tablonun dış hatlarına yeşil kenarlıklar ekleyin.
table.set_border(aw.BorderType.LEFT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.RIGHT, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.TOP, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
table.set_border(aw.BorderType.BOTTOM, aw.LineStyle.SINGLE, 1.5, aspose.pydrawing.Color.green, True)
# Hücreleri açık yeşil katı bir renk ile doldurun.
table.set_shading(aw.TextureIndex.TEXTURE_SOLID, aspose.pydrawing.Color.light_green, aspose.pydrawing.Color.empty())
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetOutlineBorders.docx')
```

### See Also

* module [aspose.words.tables](../)

