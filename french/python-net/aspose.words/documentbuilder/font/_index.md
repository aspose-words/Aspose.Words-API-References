---
title: DocumentBuilder.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "DocumentBuilder.font property. Returns an object that represents current font formatting properties."
type: docs
weight: 100
url: /fr/python-net/aspose.words/documentbuilder/font/
---

## DocumentBuilder.font property

Returns an object that represents current font formatting properties.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

Use [DocumentBuilder.font](./) to access and modify font formatting properties.

Specify font formatting before inserting text.




### Examples

Shows how to insert a string surrounded by a border into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.border.color = aspose.pydrawing.Color.green
builder.font.border.line_width = 2.5
builder.font.border.line_style = aw.LineStyle.DASH_DOT_STROKER
builder.write('Text surrounded by green border.')
doc.save(file_name=ARTIFACTS_DIR + 'Border.FontBorder.docx')
```

Shows how to create a formatted table using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
table.left_indent = 20
# Définir quelques options de mise en forme pour l'apparence du texte et du tableau.
builder.row_format.height = 40
builder.row_format.height_rule = aw.HeightRule.AT_LEAST
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.from_argb(198, 217, 241)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.font.size = 16
builder.font.name = 'Arial'
builder.font.bold = True
# Configurer les options de mise en forme dans un constructeur de document les appliquera
# à la cellule/ligne actuelle où se trouve son curseur,
# ainsi qu'à toutes les nouvelles cellules et lignes créées à l'aide de ce constructeur.
builder.write('Header Row,\n Cell 1')
builder.insert_cell()
builder.write('Header Row,\n Cell 2')
builder.insert_cell()
builder.write('Header Row,\n Cell 3')
builder.end_row()
# Reconfigurer les objets de mise en forme du constructeur pour les nouvelles lignes et cellules que nous allons créer.
# Le constructeur n'appliquera pas ceux-ci à la première ligne déjà créée afin qu'elle se démarque comme ligne d'en-tête.
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.white
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.row_format.height = 30
builder.row_format.height_rule = aw.HeightRule.AUTO
builder.insert_cell()
builder.font.size = 12
builder.font.bold = False
builder.write('Row 1, Cell 1.')
builder.insert_cell()
builder.write('Row 1, Cell 2.')
builder.insert_cell()
builder.write('Row 1, Cell 3.')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, Cell 1.')
builder.insert_cell()
builder.write('Row 2, Cell 2.')
builder.insert_cell()
builder.write('Row 2, Cell 3.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.CreateFormattedTable.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

