---
title: HorizontalRuleFormat.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Ausrichtungseigenschaft „HorizontalRuleFormat“, um die Ausrichtung horizontaler Linien für mehr Designflexibilität einfach anzupassen.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Ruft die Ausrichtung der horizontalen Linie ab oder legt sie fest.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

## Bemerkungen

Der Standardwert istLeft.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
