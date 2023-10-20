---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.HorizontalRuleFormat klas. Stellt die horizontale Regelformatierung dar in C#.
type: docs
weight: 1050
url: /de/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Stellt die horizontale Regelformatierung dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Formen](https://docs.aspose.com/words/net/working-with-shapes/) Dokumentationsartikel.

```csharp
public class HorizontalRuleFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Ruft die Ausrichtung der horizontalen Regel ab oder legt sie fest. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Ruft die Pinselfarbe ab, die die horizontale Regel ausfüllt, oder legt diese fest. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Ruft die Höhe der horizontalen Regel ab oder legt sie fest. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Zeigt das Vorhandensein einer 3D-Schattierung für die horizontale Regel an. Wenn`WAHR` dann ist die horizontale Regel ohne 3D-Schattierung und es wird Volltonfarbe verwendet. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Ruft die Länge der angegebenen horizontalen Linie, ausgedrückt als Prozentsatz der Fensterbreite, ab oder legt diese fest. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
