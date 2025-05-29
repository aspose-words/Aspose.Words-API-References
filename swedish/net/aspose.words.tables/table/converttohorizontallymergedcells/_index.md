---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words för .NET
description: Upptäck hur metoden ConvertToHorizontallyMergedCells omvandlar breda sammanfogade celler till horisontellt sammanfogade celler, vilket förbättrar din dataorganisation.
type: docs
weight: 410
url: /sv/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Konverterar celler som sammanfogats horisontellt efter bredd till celler som sammanfogats efter[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Anmärkningar

Tabellceller kan sammanfogas horisontellt med hjälp av sammanfogningsflaggor[`HorizontalMerge`](../../cellformat/horizontalmerge/) eller med hjälp av cellbredd[`Width`](../../cellformat/width/).

När tabellceller sammanfogas med width-egenskapen[`HorizontalMerge`](../../cellformat/horizontalmerge/) är meningslöst men ibland är det ett bekvämare sätt att ha sammanslagningsflaggor.

Använd den här metoden för att omvandla tabellceller som är horisontellt sammanfogade efter bredd till celler som är sammanfogade med sammanfogningsflaggor.

## Exempel

Visar hur man konverterar celler som sammanfogats horisontellt efter bredd till celler som sammanfogats med CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word skriver inte längre sammanslagningsflaggor, utan definierar istället sammanslagna celler efter bredd.
// Aspose.Words definierar som standard endast 5 celler i rad, och ingen av dem har den horisontella sammanfogningsflaggan,
// trots att det fanns 7 celler i raden innan den horisontella sammanfogningen ägde rum.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Använd metoden "ConvertToHorizontallyMergedCells" för att konvertera celler som är horisontellt sammanfogade
// av dess bredd till cellen horisontellt sammanfogad med flaggor.
// Nu har vi 7 celler, och några av dem har horisontella sammanfogningsvärden.
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

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
