---
title: TabStopCollection.After
linktitle: After
articleTitle: After
second_title: Aspose.Words per .NET
description: Scopri il metodo TabStopCollection After per recuperare in modo efficiente la prima tabulazione a destra della posizione specificata per una navigazione fluida.
type: docs
weight: 40
url: /it/net/aspose.words/tabstopcollection/after/
---
## TabStopCollection.After method

Ottiene una prima tabulazione a destra della posizione specificata.

```csharp
public TabStop After(double position)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| position | Double | La posizione di riferimento (in punti). |

### Valore di ritorno

Un oggetto di tabulazione o`null` se non è stata trovata una tabulazione adatta.

## Osservazioni

Salta le tabulazioni con[`Alignment`](../../tabstop/alignment/) impostato suBar.

## Esempi

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 punti equivalgono a un "pollice" sul righello delle tabulazioni di Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Ogni carattere "tab" sposta il cursore del builder nella posizione della tabulazione successiva.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Ogni paragrafo ottiene la sua raccolta di tabulazioni, che clona i suoi valori dalla raccolta di tabulazioni del generatore di documenti.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Una raccolta di tabulazioni può indicarci i TabStop prima e dopo determinate posizioni.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Possiamo cancellare l'insieme delle tabulazioni di un paragrafo per ripristinare il comportamento di tabulazione predefinito.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Guarda anche

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
