---
title: LineStyle Enum
linktitle: LineStyle
articleTitle: LineStyle
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.LineStyle 枚举. 指定 a 的线型Border 在 C#.
type: docs
weight: 3450
url: /zh/net/aspose.words/linestyle/
---
## LineStyle enumeration

指定 a 的线型[`Border`](../border/).

```csharp
public enum LineStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
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

## 例子

演示如何将由边框包围的字符串插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
