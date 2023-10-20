---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words für .NET
description: HorizontalRuleFormat WidthPercent eigendom. Ruft die Länge der angegebenen horizontalen Linie ausgedrückt als Prozentsatz der Fensterbreite ab oder legt diese fest in C#.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Ruft die Länge der angegebenen horizontalen Linie, ausgedrückt als Prozentsatz der Fensterbreite, ab oder legt diese fest.

```csharp
public double WidthPercent { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

## Bemerkungen

Gültige Werte reichen von 1 bis einschließlich 100.

Der Standardwert ist 100.

## Beispiele

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
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
