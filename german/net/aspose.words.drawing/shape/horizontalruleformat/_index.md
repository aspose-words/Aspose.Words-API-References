---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words für .NET
description: Greifen Sie auf die HorizontalRuleFormat-Eigenschaften zu und passen Sie sie an, um mehr Gestaltungsflexibilität zu erhalten. Optimieren Sie Ihre Formen mit maßgeschneiderten Einstellungen für einzigartige Ergebnisse.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Bietet Zugriff auf die Eigenschaften der horizontalen Linienform. Gibt für eine Form, die keine horizontale Linie ist, Folgendes zurück:`null` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
```

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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
