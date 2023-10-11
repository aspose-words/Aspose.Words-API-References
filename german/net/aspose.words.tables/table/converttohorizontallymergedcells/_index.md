---
title: Table.ConvertToHorizontallyMergedCells
second_title: Aspose.Words für .NET-API-Referenz
description: Table methode. Konvertiert horizontal um die Breite verbundene Zellen in um zusammengeführte ZellenHorizontalMerge .
type: docs
weight: 410
url: /de/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Konvertiert horizontal um die Breite verbundene Zellen in um zusammengeführte Zellen[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

### Bemerkungen

Tabellenzellen können entweder mithilfe von Merge-Flags horizontal zusammengeführt werden[`HorizontalMerge`](../../cellformat/horizontalmerge/) oder mit der Zellenbreite[`Width`](../../cellformat/width/).

Wenn eine Tabellenzelle durch die Eigenschaft „Breite“ zusammengeführt wird[`HorizontalMerge`](../../cellformat/horizontalmerge/) ist bedeutungslos, aber manchmal ist es bequemer, Merge-Flags zu haben.

Verwenden Sie diese Methode, um horizontal nach der Breite zusammengeführte Tabellenzellen in durch Zusammenführungsflags zusammengeführte Zellen umzuwandeln.

### Beispiele

Zeigt, wie horizontal nach Breite zusammengeführte Zellen in durch CellFormat.HorizontalMerge zusammengeführte Zellen konvertiert werden.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word schreibt keine Zusammenführungsflags mehr, sondern definiert zusammengeführte Zellen stattdessen nach der Breite.
// Aspose.Words definiert standardmäßig nur 5 Zellen in einer Zeile und keine davon verfügt über die Flagge für die horizontale Zusammenführung.
// obwohl sich vor der horizontalen Zusammenführung 7 Zellen in der Zeile befanden.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Verwenden Sie die Methode „ConvertToHorizontallyMergedCells“, um horizontal zusammengeführte Zellen zu konvertieren
// um seine Breite zur horizontal durch Flags zusammengeführten Zelle.
// Jetzt haben wir 7 Zellen und einige davon haben horizontale Zusammenführungswerte.
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

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


