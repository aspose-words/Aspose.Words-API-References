---
title: TableStyleOptions enumeration
linktitle: TableStyleOptions enumeration
articleTitle: TableStyleOptions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.TableStyleOptions enumeration. Specifies how table style is applied to a table."
type: docs
weight: 150
url: /ar/python-net/aspose.words.tables/tablestyleoptions/
---

## TableStyleOptions enumeration

Specifies how table style is applied to a table.


### Members

| Name | Description |
| --- | --- |
| NONE | No table style formatting is applied. |
| FIRST_ROW | Apply first row conditional formatting. |
| LAST_ROW | Apply last row conditional formatting. |
| FIRST_COLUMN | Apply 1 first column conditional formatting. |
| LAST_COLUMN | Apply last column conditional formatting. |
| ROW_BANDS | Apply row banding conditional formatting. |
| COLUMN_BANDS | Apply column banding conditional formatting. |
| DEFAULT2003 | Row and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF. |
| DEFAULT | This is Microsoft Word defaults. |

### Examples

Shows how to build a new table while applying a style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# يجب أن ندرج صفًا واحدًا على الأقل قبل ضبط أي تنسيق للجدول.
builder.insert_cell()
# حدد نمط الجدول المستخدم بناءً على معرف النمط.
# لاحظ أن ليس كل أنماط الجداول متاحة عند الحفظ بتنسيق .doc.
table.style_identifier = aw.StyleIdentifier.MEDIUM_SHADING1_ACCENT1
# طبق النمط جزئيًا على ميزات الجدول بناءً على الشروط، ثم أنشئ الجدول.
table.style_options = aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS | aw.tables.TableStyleOptions.FIRST_ROW
table.auto_fit(aw.tables.AutoFitBehavior.AUTO_FIT_TO_CONTENTS)
builder.writeln('Item')
builder.cell_format.right_padding = 40
builder.insert_cell()
builder.writeln('Quantity (kg)')
builder.end_row()
builder.insert_cell()
builder.writeln('Apples')
builder.insert_cell()
builder.writeln('20')
builder.end_row()
builder.insert_cell()
builder.writeln('Bananas')
builder.insert_cell()
builder.writeln('40')
builder.end_row()
builder.insert_cell()
builder.writeln('Carrots')
builder.insert_cell()
builder.writeln('50')
builder.end_row()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTableWithStyle.docx')
```

### See Also

* module [aspose.words.tables](../)
* property [Table.style_options](../table/style_options/)

