---
title: HorizontalRuleAlignment Enum
linktitle: HorizontalRuleAlignment
articleTitle: HorizontalRuleAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.HorizontalRuleAlignment für eine präzise Kontrolle über die horizontale Linienausrichtung und verbessern Sie so die Formatierung und das Design Ihres Dokuments.
type: docs
weight: 1370
url: /de/net/aspose.words.drawing/horizontalrulealignment/
---
## HorizontalRuleAlignment enumeration

Stellt die Ausrichtung für die angegebene horizontale Linie dar.

```csharp
public enum HorizontalRuleAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Left | `0` | Linksbündig. |
| Center | `1` | Mittig ausgerichtet. |
| Right | `2` | Rechtsbündig. |

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
