---
title: DocumentBuilder.end_row method
linktitle: end_row method
articleTitle: end_row method
second_title: Aspose.Words for Python
description: "DocumentBuilder.end_row method. Ends a table row in the document."
type: docs
weight: 240
url: /it/python-net/aspose.words/documentbuilder/end_row/
---

## end_row() {#default}

Ends a table row in the document.


```python
def end_row(self):
    ...
```

### Remarks

Call [DocumentBuilder.end_row()](./#default) to end a table row. If you call [DocumentBuilder.insert_cell()](../insert_cell/#default) immediately
after that, then the table continues on a new row.

Use the [DocumentBuilder.row_format](../row_format/) property to specify row formatting.




### Returns

The row node that was just finished.


### Examples

Shows how to merge table cells vertically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserisci una cella nella prima colonna della prima riga.
# Questa cella sarà la prima in un intervallo di celle unite verticalmente.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.FIRST
builder.write('Text in merged cells.')
# Inserisci una cella nella seconda colonna della prima riga, quindi termina la riga.
# Inoltre, configura il builder per disabilitare l'unione verticale nelle celle create.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
# Inserisci una cella nella prima colonna della seconda riga.
# Invece di aggiungere contenuti di testo, uniremo questa cella con la prima cella che abbiamo aggiunto direttamente sopra.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.PREVIOUS
# Inserisci un'altra cella indipendente nella seconda colonna della seconda riga.
builder.insert_cell()
builder.cell_format.vertical_merge = aw.tables.CellMerge.NONE
builder.write('Text in unmerged cell.')
builder.end_row()
builder.end_table()
doc.save(file_name=ARTIFACTS_DIR + 'CellFormat.VerticalMerge.docx')
```

Shows how to build a table with custom borders.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
# Impostazione delle opzioni di formattazione della tabella per un document builder
# le applicherà a ogni riga e cella che aggiungiamo con esso.
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
# Modificare la formattazione la applicherà alla cella corrente,
# e tutte le nuove celle che creiamo con il builder in seguito.
# Questo non influenzerà le celle che abbiamo aggiunto in precedenza.
builder.cell_format.shading.clear_formatting()
builder.insert_cell()
builder.write('Row 2, Col 1')
builder.insert_cell()
builder.write('Row 2, Col 2')
builder.end_row()
# Aumenta l'altezza della riga per adattarla al testo verticale.
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

Shows how to build a formatted 2x2 table.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.cell_format.vertical_alignment = aw.tables.CellVerticalAlignment.CENTER
builder.write('Row 1, cell 1.')
builder.insert_cell()
builder.write('Row 1, cell 2.')
builder.end_row()
# Durante la creazione della tabella, il document builder applicherà i valori correnti delle proprietà RowFormat/CellFormat
# alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che le crea.
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[0].cell_format.vertical_alignment)
self.assertEqual(aw.tables.CellVerticalAlignment.CENTER, table.rows[0].cells[1].cell_format.vertical_alignment)
builder.insert_cell()
builder.row_format.height = 100
builder.row_format.height_rule = aw.HeightRule.EXACTLY
builder.cell_format.orientation = aw.TextOrientation.UPWARD
builder.write('Row 2, cell 1.')
builder.insert_cell()
builder.cell_format.orientation = aw.TextOrientation.DOWNWARD
builder.write('Row 2, cell 2.')
builder.end_row()
builder.end_table()
# Le righe e le celle aggiunte in precedenza non sono retroattivamente influenzate dalle modifiche al formato del builder.
self.assertEqual(0, table.rows[0].row_format.height)
self.assertEqual(aw.HeightRule.AUTO, table.rows[0].row_format.height_rule)
self.assertEqual(100, table.rows[1].row_format.height)
self.assertEqual(aw.HeightRule.EXACTLY, table.rows[1].row_format.height_rule)
self.assertEqual(aw.TextOrientation.UPWARD, table.rows[1].cells[0].cell_format.orientation)
self.assertEqual(aw.TextOrientation.DOWNWARD, table.rows[1].cells[1].cell_format.orientation)
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.BuildTable.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

