---
title: HorizontalRuleFormat.Color
second_title: Aspose.Words für .NET-API-Referenz
description: HorizontalRuleFormat eigendom. Ruft die Pinselfarbe ab die die horizontale Regel ausfüllt oder legt diese fest.
type: docs
weight: 20
url: /de/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Ruft die Pinselfarbe ab, die die horizontale Regel ausfüllt, oder legt diese fest.

```csharp
public Color Color { get; set; }
```

### Bemerkungen

Dies ist eine Verknüpfung zum[`Color`](../../fill/color/) Eigentum.

Der Standardwert ist Gray.

### Beispiele

Zeigt, wie man eine horizontale Regelform einfügt und deren Formatierung anpasst.

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
* namensraum [Aspose.Words.Drawing](../../horizontalruleformat/)
* Montage [Aspose.Words](../../../)


