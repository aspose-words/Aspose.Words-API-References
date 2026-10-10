---
title: BorderCollection.left property
linktitle: left property
articleTitle: left property
second_title: Aspose.Words for Python
description: "BorderCollection.left property. Gets the left border."
type: docs
weight: 70
url: /fr/python-net/aspose.words/bordercollection/left/
---

## BorderCollection.left property

Gets the left border.


```python
@property
def left(self) -> aspose.words.Border:
    ...

```

### Examples

Shows how to apply border and shading color while building a table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Démarrez un tableau et définissez une couleur/épaisseur par défaut pour ses bordures.
table = builder.start_table()
table.set_borders(aw.LineStyle.SINGLE, 2, aspose.pydrawing.Color.black)
# Créez une ligne avec deux cellules ayant des couleurs d'arrière-plan différentes.
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.light_sky_blue
builder.writeln('Row 1, Cell 1.')
builder.insert_cell()
builder.cell_format.shading.background_pattern_color = aspose.pydrawing.Color.orange
builder.writeln('Row 1, Cell 2.')
builder.end_row()
# Réinitialisez le formatage des cellules pour désactiver les couleurs d'arrière-plan
# définissez une épaisseur de bordure personnalisée pour toutes les nouvelles cellules créées par le constructeur,
# puis construisez une deuxième ligne.
builder.cell_format.clear_formatting()
builder.cell_format.borders.left.line_width = 4
builder.cell_format.borders.right.line_width = 4
builder.cell_format.borders.top.line_width = 4
builder.cell_format.borders.bottom.line_width = 4
builder.insert_cell()
builder.writeln('Row 2, Cell 1.')
builder.insert_cell()
builder.writeln('Row 2, Cell 2.')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.TableBordersAndShading.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

