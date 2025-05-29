---
title: Shape.HorizontalRuleFormat
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words per .NET
description: Accedi e personalizza le proprietà di HorizontalRuleFormat per una maggiore flessibilità di progettazione. Ottimizza le tue forme con impostazioni personalizzate per risultati unici.
type: docs
weight: 110
url: /it/net/aspose.words.drawing/shape/horizontalruleformat/
---
## Shape.HorizontalRuleFormat property

Fornisce l'accesso alle proprietà della forma della regola orizzontale. Per una forma che non è una regola orizzontale, restituisce`null` .

```csharp
public HorizontalRuleFormat HorizontalRuleFormat { get; }
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

* class [HorizontalRuleFormat](../../horizontalruleformat/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
