---
title: Enum LineStyle
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.LineStyle Sıralama. Bir çizgi stilini belirtirBorder .
type: docs
weight: 3450
url: /tr/net/aspose.words/linestyle/
---
## LineStyle enumeration

Bir çizgi stilini belirtir[`Border`](../border/) .

```csharp
public enum LineStyle
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Thick | `2` |  |
| Double | `3` |  |
| Hairline | `5` |  |
| Dot | `6` |  |
| DashLargeGap | `7` |  |
| DotDash | `8` |  |
| DotDotDash | `9` |  |
| Triple | `10` |  |
| ThinThickSmallGap | `11` |  |
| ThickThinSmallGap | `12` |  |
| ThinThickThinSmallGap | `13` |  |
| ThinThickMediumGap | `14` |  |
| ThickThinMediumGap | `15` |  |
| ThinThickThinMediumGap | `16` |  |
| ThinThickLargeGap | `17` |  |
| ThickThinLargeGap | `18` |  |
| ThinThickThinLargeGap | `19` |  |
| Wave | `20` |  |
| DoubleWave | `21` |  |
| DashSmallGap | `22` |  |
| DashDotStroker | `23` |  |
| Emboss3D | `24` |  |
| Engrave3D | `25` |  |
| Outset | `26` |  |
| Inset | `27` |  |

### Örnekler

Kenarlıkla çevrelenmiş bir dizenin belgeye nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


