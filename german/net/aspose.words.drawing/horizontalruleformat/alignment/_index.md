---
title: HorizontalRuleFormat.Alignment
second_title: Aspose.Words für .NET-API-Referenz
description: HorizontalRuleFormat eigendom. Ruft die Ausrichtung der horizontalen Regel ab oder legt sie fest.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Ruft die Ausrichtung der horizontalen Regel ab oder legt sie fest.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

### Bemerkungen

Der Standardwert istLeft.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* namensraum [Aspose.Words.Drawing](../../horizontalruleformat/)
* Montage [Aspose.Words](../../../)


