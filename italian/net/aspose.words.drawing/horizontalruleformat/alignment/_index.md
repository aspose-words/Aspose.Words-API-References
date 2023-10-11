---
title: HorizontalRuleFormat.Alignment
second_title: Aspose.Words per .NET API Reference
description: HorizontalRuleFormat proprietà. Ottiene o imposta lallineamento della linea orizzontale.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/horizontalruleformat/alignment/
---
## HorizontalRuleFormat.Alignment property

Ottiene o imposta l'allineamento della linea orizzontale.

```csharp
public HorizontalRuleAlignment Alignment { get; set; }
```

### Osservazioni

Il valore predefinito èLeft.

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

* enum [HorizontalRuleAlignment](../../horizontalrulealignment/)
* class [HorizontalRuleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../horizontalruleformat/)
* assemblea [Aspose.Words](../../../)


