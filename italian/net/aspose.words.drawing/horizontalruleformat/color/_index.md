---
title: HorizontalRuleFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words per .NET
description: Scopri la proprietà Colore HorizontalRuleFormat per personalizzare il tuo design. Imposta o ottieni facilmente il colore del pennello per uno straordinario effetto riga orizzontale!
type: docs
weight: 20
url: /it/net/aspose.words.drawing/horizontalruleformat/color/
---
## HorizontalRuleFormat.Color property

Ottiene o imposta il colore del pennello che riempie la regola orizzontale.

```csharp
public Color Color { get; set; }
```

## Osservazioni

Questa è una scorciatoia per[`Color`](../../fill/color/) proprietà.

Il valore predefinito è Gray .

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

* class [HorizontalRuleFormat](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
