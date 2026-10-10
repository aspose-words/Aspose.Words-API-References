---
title: Table.style_options property
linktitle: style_options property
articleTitle: style_options property
second_title: Aspose.Words for Python
description: "Table.style_options property. Gets or sets bit flags that specify how a table style is applied to this table."
type: docs
weight: 300
url: /fr/python-net/aspose.words.tables/table/style_options/
---

## Table.style_options property

Gets or sets bit flags that specify how a table style is applied to this table.


```python
@property
def style_options(self) -> aspose.words.tables.TableStyleOptions:
    ...

@style_options.setter
def style_options(self, value: aspose.words.tables.TableStyleOptions):
    ...

```

### Examples

Shows how to build a new table while applying a style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
# Nous devons insérer au moins une ligne avant de définir tout formatage de tableau.
builder.insert_cell()
# Définissez le style de tableau utilisé en fonction de l'identifiant du style.
# Notez que tous les styles de tableau ne sont pas disponibles lors de l'enregistrement au format .doc.
table.style_identifier = aw.StyleIdentifier.MEDIUM_SHADING1_ACCENT1
# Appliquez partiellement le style aux caractéristiques du tableau en fonction de prédicats, puis construisez le tableau.
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

* module [aspose.words.tables](../../)
* class [Table](../)

