---
title: HorizontalRuleFormat.Color
second_title: Aspose.Words per .NET API Reference
description: HorizontalRuleFormat proprietà. Ottiene o imposta il colore del pennello che riempie il filetto orizzontale.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Ottiene o imposta il colore del pennello che riempie il filetto orizzontale.

```csharp
public Color Color { get; set; }
```

### Osservazioni

Questa è una scorciatoia per[`Color`](../../fill/color/) proprietà.

Il valore predefinito è Gray.

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


