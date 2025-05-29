---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words per .NET
description: Scopri il metodo ShapeText di iTextShaper, che genera in modo efficiente oggetti Cluster da frammenti di testo, garantendo una formattazione e un allineamento del testo precisi.
type: docs
weight: 10
url: /it/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Restituisce[`Cluster`](../../cluster/)oggetti generati da una sequenza di frammenti di testo. La lunghezza dell'array restituito è uguale alla lunghezza di*runs* . Se l'esecuzione su un indice presenta cluster corrispondenti, il risultato sullo stesso indice li registrerà.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| runs | String[] | Una sequenza di frammenti di testo |
| direction | Direction | Una direzione del testo |
| script | UnicodeScript | Una sceneggiatura |
| enabledFontFeatures | FontFeature[] | Un set di funzionalità OpenType esplicitamente abilitate da considerare |
| variations | VariationAxisCoordinate[] | Valori dell'asse di variazione del font |

### Guarda anche

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* spazio dei nomi [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* assemblea [Aspose.Words](../../../)
