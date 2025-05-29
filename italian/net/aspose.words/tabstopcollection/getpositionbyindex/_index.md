---
title: TabStopCollection.GetPositionByIndex
linktitle: GetPositionByIndex
articleTitle: GetPositionByIndex
second_title: Aspose.Words per .NET
description: Scopri il metodo GetPositionByIndex di TabStopCollection per trovare facilmente le posizioni delle tabulazioni in base all'indice. Ottimizza il tuo layout senza sforzo!
type: docs
weight: 100
url: /it/net/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection.GetPositionByIndex method

Ottiene la posizione (in punti) della tabulazione all'indice specificato.

```csharp
public double GetPositionByIndex(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Un indice nella raccolta delle tabulazioni. |

### Valore di ritorno

La posizione della tabulazione.

## Esempi

Mostra come trovare una scheda, fermarsi al suo indice e verificarne la posizione.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

// Verifica la posizione della seconda tabulazione nella raccolta.
Assert.AreEqual(ConvertUtil.MillimeterToPoint(60), tabStops.GetPositionByIndex(1), 0.1d);
```

### Guarda anche

* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
