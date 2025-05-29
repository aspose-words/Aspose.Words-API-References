---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.BorderType-enum för anpassningsbara kantlinjer. Förbättra dina dokument med exakt kantkontroll och stil!
type: docs
weight: 290
url: /sv/net/aspose.words/bordertype/
---
## BorderType enumeration

Anger sidorna av en kantlinje.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public enum BorderType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `-1` | Standardvärde. |
| Bottom | `0` | Anger den nedre kanten av ett stycke eller en tabellcell. |
| Left | `1` | Anger den vänstra kanten för ett stycke eller en tabellcell. |
| Right | `2` | Anger den högra kanten för ett stycke eller en tabellcell. |
| Top | `3` | Anger den övre kanten av ett stycke eller en tabellcell. |
| Horizontal | `4` | Anger den horisontella kantlinjen mellan celler i en tabell eller mellan överensstämmande stycken. |
| Vertical | `5` | Anger den vertikala kantlinjen mellan celler i en tabell. |
| DiagonalDown | `6` | Anger den diagonala kantlinjen i en tabellcell. |
| DiagonalUp | `7` | Anger den diagonala kantlinjen i en tabellcell. |

## Exempel

Visar hur man infogar ett stycke med en övre kantlinje.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Ställ endast in ThemeColor när LineWidth eller LineStyle är inställda.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
