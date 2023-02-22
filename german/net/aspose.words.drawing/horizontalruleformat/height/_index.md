---
title: HorizontalRuleFormat.Height
second_title: Aspose.Words für .NET-API-Referenz
description: HorizontalRuleFormat eigendom. Ruft die Höhe der horizontalen Linie ab oder legt sie fest.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Ruft die Höhe der horizontalen Linie ab oder legt sie fest.

```csharp
public double Height { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des gültigen Wertebereichs lag. |

### Bemerkungen

Dies ist eine Verknüpfung zum[`Height`](../../shapebase/height/) Eigentum.

Gültige Werte reichen von 0 bis einschließlich 1584.

Der Standardwert ist 1,5.

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


