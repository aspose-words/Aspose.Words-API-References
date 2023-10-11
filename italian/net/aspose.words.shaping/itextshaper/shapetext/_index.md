---
title: ITextShaper.ShapeText
second_title: Aspose.Words per .NET API Reference
description: ITextShaper metodo. RestituisceClusteroggetti generati da una sequenza di frammenti di testo. La lunghezza dellarray restituito è uguale alla lunghezza diruns . Se lesecuzione su un indice ha cluster corrispondenti il risultato sullo stesso indice li registrerà.
type: docs
weight: 10
url: /it/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Restituisce[`Cluster`](../../cluster/)oggetti generati da una sequenza di frammenti di testo. La lunghezza dell'array restituito è uguale alla lunghezza di*runs* . Se l'esecuzione su un indice ha cluster corrispondenti, il risultato sullo stesso indice li registrerà.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| runs | String[] | Una sequenza di frammenti di testo |
| direction | Direction | Una direzione del testo |
| script | UnicodeScript | Un copione |
| fontFeatures | FontFeature[] | Una serie di caratteristiche da considerare |

### Guarda anche

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* spazio dei nomi [Aspose.Words.Shaping](../../itextshaper/)
* assemblea [Aspose.Words](../../../)


