---
title: HorizontalRuleFormat.Height
linktitle: Height
articleTitle: Height
second_title: Aspose.Words per .NET
description: Regola facilmente l'altezza della tua riga orizzontale. Esplora la proprietà Altezza per personalizzare il design dei tuoi progetti web. Migliora il tuo layout oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.drawing/horizontalruleformat/height/
---
## HorizontalRuleFormat.Height property

Ottiene o imposta l'altezza della regola orizzontale.

```csharp
public double Height { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Generato quando l'argomento non rientra nell'intervallo di valori validi. |

## Osservazioni

Questa è una scorciatoia per[`Height`](../../shapebase/height/) proprietà.

I valori validi vanno da 0 a 1584 inclusi.

Il valore predefinito è 1,5.

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
