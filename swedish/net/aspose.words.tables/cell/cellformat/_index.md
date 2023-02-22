---
title: Cell.CellFormat
second_title: Aspose.Words för .NET API Referens
description: Cell fast egendom. Ger tillgång till cellens formateringsegenskaper.
type: docs
weight: 20
url: /sv/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Ger tillgång till cellens formateringsegenskaper.

```csharp
public CellFormat CellFormat { get; }
```

### Exempel

Visar hur man ändrar formateringen av en tabellcell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Använd en cells "CellFormat"-egenskap för att ställa in formatering som ändrar cellens utseende.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Visar hur man kombinerar raderna från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan finns två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tables" för en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Med "GetChild"-metoden:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägg till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma bordsbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

Visar hur du ändrar formatet för rader och celler i en tabell.

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
// av innehållet i alla celler i den här raden.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Använd egenskapen "CellFormat" för den första cellen i den sista raden för att ändra formateringen av cellens innehåll.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Se även

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* namnutrymme [Aspose.Words.Tables](../../cell/)
* hopsättning [Aspose.Words](../../../)


