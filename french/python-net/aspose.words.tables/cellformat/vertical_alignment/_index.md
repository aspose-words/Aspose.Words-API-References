---
title: CellFormat.vertical_alignment property
linktitle: vertical_alignment property
articleTitle: vertical_alignment property
second_title: Aspose.Words for Python
description: "CellFormat.vertical_alignment property. Returns or sets the vertical alignment of text in the cell."
type: docs
weight: 120
url: /fr/python-net/aspose.words.tables/cellformat/vertical_alignment/
---

## CellFormat.vertical_alignment property

Returns or sets the vertical alignment of text in the cell.


```python
@property
def vertical_alignment(self) -> aspose.words.tables.CellVerticalAlignment:
    ...

@vertical_alignment.setter
def vertical_alignment(self, value: aspose.words.tables.CellVerticalAlignment):
    ...

```

### Examples

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Définir les options de mise en forme du tableau pour un constructeur de document
# les appliquera à chaque ligne et cellule que nous ajoutons avec celui-ci.
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.cell_format.clear_formatting()
builder.cell_format.width = 150
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.green_yellow
builder.cell_format.wrap_text = False
builder.cell_format.fit_text = True
builder.row_format.clear_formatting()
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.row_format.height = 50
builder.row_format.borders.line_style = aw.LineStyle.ENGRAVE_3D
builder.row_format.borders.color = aspose.pydrawing.Color.orange
builder.insert_cell()
builder.write('Row 1, Col 1')
builder.insert_cell()
builder.write('Row 1, Col 2')
builder.end_row()
# Modifier la mise en forme l'appliquera à la cellule actuelle,
# et toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
# Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Augmentez la hauteur de la ligne pour s'adapter au texte vertical.
builder.insert_cell()
builder.row_format.height = 150
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 3, Col 1')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 3, Col 2')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertTable.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [CellFormat](../)

