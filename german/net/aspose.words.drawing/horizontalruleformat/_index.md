---
title: Class HorizontalRuleFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.HorizontalRuleFormat klas. Repräsentiert horizontale Linienformatierung.
type: docs
weight: 920
url: /de/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Repräsentiert horizontale Linienformatierung.

```csharp
public class HorizontalRuleFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Ruft die Ausrichtung der horizontalen Linie ab oder legt sie fest. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Ruft die Pinselfarbe ab oder legt sie fest, die die horizontale Linie ausfüllt. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Ruft die Höhe der horizontalen Linie ab oder legt sie fest. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Zeigt das Vorhandensein von 3D-Schattierung für die horizontale Linie an. Wenn wahr, dann ist die horizontale Linie ohne 3D-Schattierung und es wird Volltonfarbe verwendet. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Ruft die Länge der angegebenen horizontalen Linie ab oder legt sie fest, ausgedrückt als Prozentsatz der Fensterbreite. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


