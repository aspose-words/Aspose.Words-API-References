---
title: Table.ClearBorders
linktitle: ClearBorders
articleTitle: ClearBorders
second_title: Aspose.Words för .NET
description: Upptäck Table ClearBorders-metoden för att enkelt ta bort alla tabell- och cellkanter, vilket förbättrar din designs tydlighet och attraktionskraft.
type: docs
weight: 390
url: /sv/net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

Tar bort alla tabell- och cellkanter i den här tabellen.

```csharp
public void ClearBorders()
```

## Exempel

Visar hur man tillämpar en konturkantlinje på en tabell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Justera tabellen till mitten av sidan.
table.Alignment = TableAlignment.Center;

// Ta bort alla befintliga ramar och skuggningar från tabellen.
table.ClearBorders();
table.ClearShading();

// Lägg till gröna ramar runt tabellens kontur.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Fyll cellerna med en ljusgrön enfärgad.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

Visar hur man tar bort alla ramar från en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

// Ändra färg och tjocklek på den övre kanten.
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// Rensa kantlinjerna för alla celler i tabellen och spara sedan dokumentet.
table.ClearBorders();
doc.Save(ArtifactsDir + "Table.ClearBorders.docx");

// Verifiera värdena för tabellens egenskaper efter att dokumentet har öppnats igen.
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
