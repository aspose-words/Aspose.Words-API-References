---
title: LineStyle Enum
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words لـ .NET
description: Aspose.Words.LineStyle تعداد. يحدد نمط الخط لـ aBorder  في C#.
type: docs
weight: 3450
url: /ar/net/aspose.words/linestyle/
---
## LineStyle enumeration

يحدد نمط الخط لـ a[`Border`](../border/) .

```csharp
public enum LineStyle
```

### قيم

| اسم | قيمة | وصف |
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

## أمثلة

يوضح كيفية إدراج سلسلة محاطة بحد في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
