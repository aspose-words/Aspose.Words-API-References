---
title: TextureIndex Enum
linktitle: TextureIndex
articleTitle: TextureIndex
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TextureIndex-enum för avancerade skuggningstexturer. Förbättra din dokumentdesign med anpassningsbara texturer av hög kvalitet.
type: docs
weight: 7300
url: /sv/net/aspose.words/textureindex/
---
## TextureIndex enumeration

Anger skuggningstextur.

```csharp
public enum TextureIndex
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Texture10Percent | `3` |  |
| Texture12Pt5Percent | `37` |  |
| Texture15Percent | `38` |  |
| Texture17Pt5Percent | `39` |  |
| Texture20Percent | `4` |  |
| Texture22Pt5Percent | `40` |  |
| Texture25Percent | `5` |  |
| Texture27Pt5Percent | `41` |  |
| Texture2Pt5Percent | `35` |  |
| Texture30Percent | `6` |  |
| Texture32Pt5Percent | `42` |  |
| Texture35Percent | `43` |  |
| Texture37Pt5Percent | `44` |  |
| Texture40Percent | `7` |  |
| Texture42Pt5Percent | `45` |  |
| Texture45Percent | `46` |  |
| Texture47Pt5Percent | `47` |  |
| Texture50Percent | `8` |  |
| Texture52Pt5Percent | `48` |  |
| Texture55Percent | `49` |  |
| Texture57Pt5Percent | `50` |  |
| Texture5Percent | `2` |  |
| Texture60Percent | `9` |  |
| Texture62Pt5Percent | `51` |  |
| Texture65Percent | `52` |  |
| Texture67Pt5Percent | `53` |  |
| Texture70Percent | `10` |  |
| Texture72Pt5Percent | `54` |  |
| Texture75Percent | `11` |  |
| Texture77Pt5Percent | `55` |  |
| Texture7Pt5Percent | `36` |  |
| Texture80Percent | `12` |  |
| Texture82Pt5Percent | `56` |  |
| Texture85Percent | `57` |  |
| Texture87Pt5Percent | `58` |  |
| Texture90Percent | `13` |  |
| Texture92Pt5Percent | `59` |  |
| Texture95Percent | `60` |  |
| Texture97Pt5Percent | `61` |  |
| TextureCross | `24` |  |
| TextureDarkCross | `18` |  |
| TextureDarkDiagonalCross | `19` |  |
| TextureDarkDiagonalDown | `16` |  |
| TextureDarkDiagonalUp | `17` |  |
| TextureDarkHorizontal | `14` |  |
| TextureDarkVertical | `15` |  |
| TextureDiagonalCross | `25` |  |
| TextureDiagonalDown | `22` |  |
| TextureDiagonalUp | `23` |  |
| TextureHorizontal | `20` |  |
| TextureNone | `0` |  |
| TextureSolid | `1` |  |
| TextureVertical | `21` |  |
| TextureNil | `65535` | Anger att inget mönster ska användas i det aktuella skuggade området (dvs. mönstret ska vara en komplett fyllning med bakgrundsfärgen). |

## Exempel

Visar hur man dekorerar text med ramar och skuggning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
