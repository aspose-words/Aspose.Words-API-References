---
title: HorizontalRuleFormat.NoShade
linktitle: NoShade
articleTitle: NoShade
second_title: Aspose.Words per .NET
description: Scopri la proprietà NoShade di HorizontalRuleFormat e controlla l'ombreggiatura 3D per le linee orizzontali. Ottieni un design elegante e dai colori uniformi senza sforzo!
type: docs
weight: 40
url: /it/net/aspose.words.drawing/horizontalruleformat/noshade/
---
## HorizontalRuleFormat.NoShade property

Indica la presenza di ombreggiatura 3D per la regola orizzontale. Se`VERO` , quindi la regola orizzontale è senza ombreggiatura 3D e viene utilizzato un colore pieno.

```csharp
public bool NoShade { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

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
