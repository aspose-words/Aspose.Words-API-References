---
title: HorizontalRuleFormat.NoShade
second_title: Aspose.Words per .NET API Reference
description: HorizontalRuleFormat proprietà. Indica la presenza dellombreggiatura 3D per la riga orizzontale. Se true la riga orizzontale è priva di ombreggiatura 3D e viene utilizzata la tinta unita.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indica la presenza dell'ombreggiatura 3D per la riga orizzontale. Se true, la riga orizzontale è priva di ombreggiatura 3D e viene utilizzata la tinta unita.

```csharp
public bool NoShade { get; set; }
```

### Osservazioni

Il valore predefinito è falso.

### Esempi

Mostra come inserire una forma di filetto orizzontale e personalizzarne la formattazione.

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

* class [HorizontalRuleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../horizontalruleformat/)
* assemblea [Aspose.Words](../../../)


