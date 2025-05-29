---
title: ShapeBase.IsHorizontalRule
linktitle: IsHorizontalRule
articleTitle: IsHorizontalRule
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase IsHorizontalRule-Eigenschaft und identifizieren Sie problemlos horizontale Linien in Ihren Designs für eine verbesserte Layout- und Stileffizienz.
type: docs
weight: 290
url: /de/net/aspose.words.drawing/shapebase/ishorizontalrule/
---
## ShapeBase.IsHorizontalRule property

Rückgaben`WAHR` wenn diese Form eine horizontale Linie ist.

```csharp
public bool IsHorizontalRule { get; }
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

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
