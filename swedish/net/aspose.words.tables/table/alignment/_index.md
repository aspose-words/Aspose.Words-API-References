---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Tabelljustering för att enkelt styra placeringen av inbäddade tabeller i dina dokument för ett elegant och professionellt utseende.
type: docs
weight: 40
url: /sv/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Anger hur en inbäddad tabell är justerad i dokumentet.

```csharp
public TableAlignment Alignment { get; set; }
```

## Anmärkningar

Standardvärdet ärLeft.

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

### Se även

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
