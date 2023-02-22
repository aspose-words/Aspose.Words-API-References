---
title: HorizontalRuleFormat.WidthPercent
second_title: Aspose.Words für .NET-API-Referenz
description: HorizontalRuleFormat eigendom. Ruft die Länge der angegebenen horizontalen Linie ab oder legt sie fest ausgedrückt als Prozentsatz der Fensterbreite.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Ruft die Länge der angegebenen horizontalen Linie ab oder legt sie fest, ausgedrückt als Prozentsatz der Fensterbreite.

```csharp
public double WidthPercent { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

### Bemerkungen

Gültige Werte reichen von 1 bis einschließlich 100.

Der Standardwert ist 100.

### Beispiele

Zeigt, wie Sie eine horizontale Linienform einfügen und ihre Formatierung anpassen.

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


