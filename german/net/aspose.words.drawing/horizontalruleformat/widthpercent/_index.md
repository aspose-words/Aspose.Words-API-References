---
title: HorizontalRuleFormat.WidthPercent
linktitle: WidthPercent
articleTitle: WidthPercent
second_title: Aspose.Words für .NET
description: Entdecken Sie die WidthPercent-Eigenschaft von HorizontalRuleFormat, um die Länge Ihrer horizontalen Linie einfach als Prozentsatz der Fensterbreite anzupassen und so eine bessere Designkontrolle zu erzielen.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/horizontalruleformat/widthpercent/
---
## HorizontalRuleFormat.WidthPercent property

Ruft die Länge der angegebenen horizontalen Linie als Prozentsatz der Fensterbreite ab oder legt sie fest.

```csharp
public double WidthPercent { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentOutOfRangeException | Wird ausgelöst, wenn das Argument außerhalb des Bereichs gültiger Werte liegt. |

## Bemerkungen

Gültige Werte reichen von 1 bis einschließlich 100.

Der Standardwert ist 100.

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
