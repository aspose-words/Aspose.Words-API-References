---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.HorizontalRuleAlignment-uppräkningen för exakt kontroll över horisontell regeljustering, vilket förbättrar formatering och design i ditt dokument.
type: docs
weight: 1370
url: /sv/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

Representerar justeringen för den angivna horisontella linjen.

```csharp
public enum HorizontalRuleAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Left | `0` | Vänsterjusterad. |
| Center | `1` | Justerad mot mitten. |
| Right | `2` | Högerjusterad. |

## Exempel

Visar hur man infogar en horisontell linjeform och anpassar dess formatering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
