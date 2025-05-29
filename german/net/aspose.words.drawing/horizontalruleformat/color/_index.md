---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Entdecken Sie die HorizontalRuleFormat-Farbeigenschaft, um Ihr Design anzupassen. Legen Sie einfach die Pinselfarbe fest oder rufen Sie sie ab, um einen beeindruckenden horizontalen Linieneffekt zu erzielen!
type: docs
weight: 20
url: /de/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Ruft die Pinselfarbe ab, mit der die horizontale Linie ausgefüllt wird, oder legt diese fest.

```csharp
public Color Color { get; set; }
```

## Bemerkungen

Dies ist eine Abkürzung zum[`Color`](../../fill/color/) Eigentum.

Der Standardwert ist Gray .

## Beispiele

Zeigt, wie Sie eine horizontale Regelform einfügen und ihre Formatierung anpassen.

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

### Siehe auch

* class [HorizontalRuleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
