---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words per .NET API Reference
description: TabStopCollection metodo. Ottiene lindice di un punto di tabulazione con la posizione specificata in punti.
type: docs
weight: 90
url: /it/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Ottiene l'indice di un punto di tabulazione con la posizione specificata in punti.

```csharp
public int GetIndexByPosition(double position)
```

### Esempi

Mostra come cercare una posizione per vedere se esiste un punto di tabulazione e ottenerne l'indice.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Aggiunge una tabulazione in una posizione di 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Un risultato di "0" restituito da "GetIndexByPosition" conferma che una tabulazione si interrompe
// a 30 mm esiste in questa raccolta ed è a indice 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Un "-1" restituito da "GetIndexByPosition" lo conferma
// non ci sono tabulazioni in questa raccolta con una posizione di 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Guarda anche

* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../tabstopcollection/)
* assemblea [Aspose.Words](../../../)


