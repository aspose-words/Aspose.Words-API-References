---
title: TableStyle.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "TableStyle.alignment property. Specifies the alignment for the table style."
type: docs
weight: 10
url: /sv/python-net/aspose.words/tablestyle/alignment/
---

## TableStyle.alignment property

Specifies the alignment for the table style.


```python
@property
def alignment(self) -> aspose.words.tables.TableAlignment:
    ...

@alignment.setter
def alignment(self, value: aspose.words.tables.TableAlignment):
    ...

```

### Remarks

The default value is [TableAlignment.LEFT](../../../aspose.words.tables/tablealignment/#LEFT).



### Examples

Shows how to set the position of a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Nedan följer två sätt att justera en tabell horisontellt.
# 1 -  Använd egenskapen "Alignment" för att placera den på en plats på sidan, till exempel i mitten:
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
table_style.alignment = aw.tables.TableAlignment.CENTER
table_style.borders.color = aspose.pydrawing.Color.blue
table_style.borders.line_style = aw.LineStyle.SINGLE
# Infoga en tabell och applicera den stil vi skapade på den.
table = builder.start_table()
builder.insert_cell()
builder.write('Aligned to the center of the page')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
table.style = table_style
# 2 -  Använd "LeftIndent" för att ange ett indrag från sidans vänstermarginal:
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle2').as_table_style()
table_style.left_indent = 55
table_style.borders.color = aspose.pydrawing.Color.green
table_style.borders.line_style = aw.LineStyle.SINGLE
table = builder.start_table()
builder.insert_cell()
builder.write('Aligned according to left indent')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
table.style = table_style
doc.save(file_name=ARTIFACTS_DIR + 'Table.SetTableAlignment.docx')
```

### See Also

* module [aspose.words](../../)
* class [TableStyle](../)

