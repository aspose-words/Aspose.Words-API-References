---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Tables.TableAlignment-enum för optimal inline-tabelljustering. Förbättra din dokumentformatering med precision och enkelhet.
type: docs
weight: 7200
url: /sv/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Anger justering för en inbäddad tabell.

```csharp
public enum TableAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Left | `0` | Tabellen är vänsterjusterad. |
| Center | `1` | Tabellen är centrerad. |
| Right | `2` | Tabellen är justerad till höger. |

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

* namnutrymme [Aspose.Words.Tables](../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../)
