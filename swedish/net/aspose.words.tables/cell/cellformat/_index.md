---
title: Cell.CellFormat
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Cell CellFormat för att enkelt komma åt och anpassa cellformateringsalternativ för förbättrad datapresentation i dina applikationer.
type: docs
weight: 20
url: /sv/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Ger åtkomst till cellens formateringsegenskaper.

```csharp
public CellFormat CellFormat { get; }
```

## Exempel

Visar hur man ändrar formateringen av en tabellcell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Använd en cells "CellFormat"-egenskap för att ange formatering som ändrar cellens utseende.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Visar hur man kombinerar rader från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan följer två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tabeller" i en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Använda metoden "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägger till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma tabellbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

Visar hur man ändrar formatet för rader och celler i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Använd den första radens "RowFormat"-egenskap för att ändra formateringen
// av innehållet i alla celler på den här raden.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Använd egenskapen "CellFormat" för den första cellen på den sista raden för att ändra formateringen av cellens innehåll.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Se även

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
