---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode ConvertToHorizontallyMergedCells breite verbundene Zellen in horizontal verbundene Zellen umwandelt und so Ihre Datenorganisation verbessert.
type: docs
weight: 410
url: /de/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Konvertiert horizontal durch Breite verbundene Zellen in Zellen, die durch[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Bemerkungen

Tabellenzellen können horizontal zusammengeführt werden, entweder durch Zusammenführungsflags[`HorizontalMerge`](../../cellformat/horizontalmerge/) oder mithilfe der Zellenbreite[`Width`](../../cellformat/width/).

Wenn Tabellenzellen durch die Breiteneigenschaft zusammengeführt werden[`HorizontalMerge`](../../cellformat/horizontalmerge/) ist bedeutungslos, aber manchmal ist es praktischer, Merge-Flags zu haben.

Verwenden Sie diese Methode, um horizontal nach Breite zusammengeführte Tabellenzellen in Zellen umzuwandeln, die nach Zusammenführungsflags zusammengeführt wurden.

## Beispiele

Zeigt, wie horizontal nach Breite verbundene Zellen in durch CellFormat.HorizontalMerge verbundene Zellen konvertiert werden.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word schreibt keine Merge-Flags mehr, sondern definiert zusammengeführte Zellen stattdessen nach der Breite.
// Aspose.Words definiert standardmäßig nur 5 Zellen in einer Zeile und keine davon hat das horizontale Zusammenführungsflag.
// obwohl vor der horizontalen Zusammenführung 7 Zellen in der Zeile waren.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Verwenden Sie die Methode "ConvertToHorizontallyMergedCells", um horizontal verbundene Zellen zu konvertieren
// durch seine Breite mit der Zelle, die horizontal durch Flags verbunden ist.
// Jetzt haben wir 7 Zellen und einige davon haben horizontal zusammengeführte Werte.
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
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
