---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.HorizontalRuleFormat für erweiterte horizontale Linienformatierung. Optimieren Sie Ihr Dokumentdesign mühelos!
type: docs
weight: 1380
url: /de/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Stellt die horizontale Linienformatierung dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Formen](https://docs.aspose.com/words/net/working-with-shapes/) Dokumentationsartikel.

```csharp
public class HorizontalRuleFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Ruft die Ausrichtung der horizontalen Linie ab oder legt sie fest. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Ruft die Pinselfarbe ab, mit der die horizontale Linie ausgefüllt wird, oder legt diese fest. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Ruft die Höhe der horizontalen Linie ab oder legt sie fest. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Zeigt das Vorhandensein einer 3D-Schattierung für die horizontale Linie an. Wenn`WAHR` , dann ist die horizontale Linie ohne 3D-Schattierung und es wird Volltonfarbe verwendet. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Ruft die Länge der angegebenen horizontalen Linie als Prozentsatz der Fensterbreite ab oder legt sie fest. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
