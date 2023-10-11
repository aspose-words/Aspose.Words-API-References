---
title: Enum TableAlignment
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Tables.TableAlignment uppräkning. Anger justering för en inlinetabell.
type: docs
weight: 6350
url: /sv/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Anger justering för en inline-tabell.

```csharp
public enum TableAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Left | `0` | Tabellen är vänsterjusterad. |
| Center | `1` | Tabellen är centrerad. |
| Right | `2` | Tabellen är högerjusterad. |

### Exempel

Visar hur man tillämpar en konturram på en tabell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Rikta in tabellen mot mitten av sidan.
table.Alignment = TableAlignment.Center;

// Rensa alla befintliga kanter och skuggningar från tabellen.
table.ClearBorders();
table.ClearShading();

// Lägg till gröna ramar till tabellens konturer.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Fyll cellerna med en ljusgrön solid färg.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Se även

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)


