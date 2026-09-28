---
title: ConditionalStyle.left_padding property
linktitle: left_padding property
articleTitle: left_padding property
second_title: Aspose.Words for Python
description: "ConditionalStyle.left_padding property. Gets or sets the amount of space (in points) to add to the left of the contents of table cells."
type: docs
weight: 40
url: /de/python-net/aspose.words/conditionalstyle/left_padding/
---

## ConditionalStyle.left_padding property

Gets or sets the amount of space (in points) to add to the left of the contents of table cells.


```python
@property
def left_padding(self) -> float:
    ...

@left_padding.setter
def left_padding(self, value: float):
    ...

```

### Examples

Shows how to work with certain area styles of a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.end_row()
builder.insert_cell()
builder.write('Cell 3')
builder.insert_cell()
builder.write('Cell 4')
builder.end_table()
# Erstelle einen benutzerdefinierten Tabellestil.
table_style = doc.styles.add(aw.StyleType.TABLE, 'MyTableStyle1').as_table_style()
# Bedingte Stile sind Formatierungsänderungen, die nur einige Zellen der Tabelle betreffen
# basierend auf einer Bedingung, wie zum Beispiel dass die Zellen in der letzten Zeile liegen.
# Unten sind drei Möglichkeiten aufgeführt, auf die bedingten Stile eines Tabellestils aus der "ConditionalStyles"-Sammlung zuzugreifen.
# 1 -  Nach Stiltyp:
table_style.conditional_styles.get_by_conditional_style_type(aw.ConditionalStyleType.FIRST_ROW).shading.background_pattern_color = drawing.Color.alice_blue
# 2 -  Nach Index:
table_style.conditional_styles[0].borders.color = drawing.Color.black
table_style.conditional_styles[0].borders.line_style = aw.LineStyle.DOT_DASH
self.assertEqual(aw.ConditionalStyleType.FIRST_ROW, table_style.conditional_styles[0].type)
# 3 -  Als Eigenschaft:
table_style.conditional_styles.first_row.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
# Wende Abstand und Textformatierung auf bedingte Stile an.
table_style.conditional_styles.last_row.bottom_padding = 10
table_style.conditional_styles.last_row.left_padding = 10
table_style.conditional_styles.last_row.right_padding = 10
table_style.conditional_styles.last_row.top_padding = 10
table_style.conditional_styles.last_column.font.bold = True
# Liste alle möglichen Stilbedingungen auf.
for style in table_style.conditional_styles:
    current_style = style
    if current_style is not None:
        print(current_style.type)
# Wende den benutzerdefinierten Stil, der alle bedingten Stile enthält, auf die Tabelle an.
table.style = table_style
# Unser Stil wendet standardmäßig einige bedingte Stile an.
self.assertEqual(aw.tables.TableStyleOptions.FIRST_ROW | aw.tables.TableStyleOptions.FIRST_COLUMN | aw.tables.TableStyleOptions.ROW_BANDS, table.style_options)
# Wir müssen alle anderen Stile selbst über die "StyleOptions"-Eigenschaft aktivieren.
table.style_options |= aw.tables.TableStyleOptions.LAST_ROW | aw.tables.TableStyleOptions.LAST_COLUMN
doc.save(file_name=ARTIFACTS_DIR + 'Table.ConditionalStyles.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConditionalStyle](../)

