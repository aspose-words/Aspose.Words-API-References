---
title: TabStopCollection.GetIndexByPosition
linktitle: GetIndexByPosition
articleTitle: GetIndexByPosition
second_title: Aspose.Words per .NET
description: Scopri il metodo GetIndexByPosition di TabStopCollection per trovare facilmente l'indice di una tabulazione in qualsiasi punto specificato. Perfetto per un controllo preciso del layout!
type: docs
weight: 90
url: /it/net/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection.GetIndexByPosition method

Ottiene l'indice di una tabulazione con la posizione specificata in punti.

```csharp
public int GetIndexByPosition(double position)
```

## Esempi

Mostra come cercare una posizione per vedere se è presente una tabulazione e ottenerne l'indice.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

// Aggiungere una tabulazione a una posizione di 30 mm.
tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);

// Un risultato di "0" restituito da "GetIndexByPosition" conferma che è stata eseguita una tabulazione
// a 30mm esiste in questa collezione e si trova all'indice 0.
Assert.AreEqual(0, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(30)));

// Un "-1" restituito da "GetIndexByPosition" conferma che
// in questa collezione non è presente alcuna tabulazione con una posizione di 60 mm.
Assert.AreEqual(-1, tabStops.GetIndexByPosition(ConvertUtil.MillimeterToPoint(60)));
```

### Guarda anche

* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
