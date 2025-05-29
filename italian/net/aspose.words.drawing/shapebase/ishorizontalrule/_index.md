---
title: ShapeBase.IsHorizontalRule
linktitle: IsHorizontalRule
articleTitle: IsHorizontalRule
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsHorizontalRule di ShapeBase e identifica facilmente le regole orizzontali nei tuoi progetti per migliorare l'efficienza di layout e stile.
type: docs
weight: 290
url: /it/net/aspose.words.drawing/shapebase/ishorizontalrule/
---
## ShapeBase.IsHorizontalRule property

Restituisce`VERO` se questa forma è una regola orizzontale.

```csharp
public bool IsHorizontalRule { get; }
```

## Esempi

Mostra come inserire una forma di regola orizzontale e personalizzarne la formattazione.

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

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
