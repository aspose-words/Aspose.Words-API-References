---
title: LineStyle Enum
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words для .NET
description: Aspose.Words.LineStyle перечисление. Определяет стиль линииBorder  на С#.
type: docs
weight: 3450
url: /ru/net/aspose.words/linestyle/
---
## LineStyle enumeration

Определяет стиль линии[`Border`](../border/) .

```csharp
public enum LineStyle
```

### Ценности

| Имя | Ценность | Описание |
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

## Примеры

Показывает, как вставить в документ строку, окруженную рамкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
