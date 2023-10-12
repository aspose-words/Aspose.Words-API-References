---
title: TabStopCollection.GetIndexByPosition
second_title: Aspose.Words per .NET API Reference
description: TabStopCollection metodo. Ottiene lindice di una tabulazione con la posizione specificata in punti.
type: docs
weight: 90
url: /it/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Ottiene l'indice di una tabulazione con la posizione specificata in punti.

```csharp
public int GetIndexByPosition(double position)
```

### Esempi

Mostra come cercare una posizione per vedere se esiste una tabulazione e ottenerne l'indice.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Aggiunge un punto di tabulazione in una posizione di 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Un risultato "0" restituito da "GetIndexByPosition" conferma che è presente un punto di tabulazione
// a 30mm esiste in questa raccolta ed è all'indice 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Un "-1" restituito da "GetIndexByPosition" lo conferma
// in questa raccolta non sono presenti tabulazioni con una posizione di 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Guarda anche

* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../tabstopcollection/)
* assemblea [Aspose.Words](../../../)


