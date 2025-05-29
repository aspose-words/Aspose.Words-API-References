---
title: HorizontalRuleFormat Class
linktitle: HorizontalRuleFormat
articleTitle: HorizontalRuleFormat
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.HorizontalRuleFormat per la formattazione avanzata delle regole orizzontali. Migliora il design dei tuoi documenti senza sforzo!
type: docs
weight: 1380
url: /it/net/aspose.words.drawing/horizontalruleformat/
---
## HorizontalRuleFormat class

Rappresenta la formattazione della regola orizzontale.

Per saperne di più, visita il[Lavorare con le forme](https://docs.aspose.com/words/net/working-with-shapes/) articolo di documentazione.

```csharp
public class HorizontalRuleFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Alignment](../../aspose.words.drawing/horizontalruleformat/alignment/) { get; set; } | Ottiene o imposta l'allineamento della regola orizzontale. |
| [Color](../../aspose.words.drawing/horizontalruleformat/color/) { get; set; } | Ottiene o imposta il colore del pennello che riempie la regola orizzontale. |
| [Height](../../aspose.words.drawing/horizontalruleformat/height/) { get; set; } | Ottiene o imposta l'altezza della regola orizzontale. |
| [NoShade](../../aspose.words.drawing/horizontalruleformat/noshade/) { get; set; } | Indica la presenza di ombreggiatura 3D per la regola orizzontale. Se`VERO` , quindi la regola orizzontale è senza ombreggiatura 3D e viene utilizzato un colore pieno. |
| [WidthPercent](../../aspose.words.drawing/horizontalruleformat/widthpercent/) { get; set; } | Ottiene o imposta la lunghezza della regola orizzontale specificata espressa come percentuale della larghezza della finestra. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
