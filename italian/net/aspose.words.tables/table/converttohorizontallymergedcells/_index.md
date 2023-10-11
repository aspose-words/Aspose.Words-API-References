---
title: Table.ConvertToHorizontallyMergedCells
second_title: Aspose.Words per .NET API Reference
description: Table metodo. Converte le celle unite orizzontalmente per larghezza in celle unite perHorizontalMerge .
type: docs
weight: 410
url: /it/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Converte le celle unite orizzontalmente per larghezza in celle unite per[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

### Osservazioni

Le celle della tabella possono essere unite orizzontalmente utilizzando i flag di unione[`HorizontalMerge`](../../cellformat/horizontalmerge/) o utilizzando la larghezza della cella[`Width`](../../cellformat/width/).

Quando la cella della tabella viene unita dalla proprietà larghezza[`HorizontalMerge`](../../cellformat/horizontalmerge/) non ha senso, ma a volte avere flag di unione è il modo più conveniente.

Utilizza questo metodo per trasformare le celle della tabella unite orizzontalmente per larghezza in celle unite tramite flag di unione.

### Esempi

Mostra come convertire le celle unite orizzontalmente per larghezza in celle unite da CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word non scrive più i flag di unione, definendo invece le celle unite in base alla larghezza.
// Aspose.Words per impostazione predefinita definisce solo 5 celle di fila e nessuna di esse ha il flag di unione orizzontale,
// anche se c'erano 7 celle nella riga prima che avvenisse la fusione orizzontale.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Utilizza il metodo "ConvertToHorizontallyMergedCells" per convertire le celle unite orizzontalmente
// per la sua larghezza alla cella unita orizzontalmente dalle bandiere.
// Ora abbiamo 7 celle e alcune di esse hanno valori di unione orizzontale.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


