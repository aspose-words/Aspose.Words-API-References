---
title: Class TabStopCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TabStopCollection classe. Una raccolta diTabStop oggetti che rappresentano schede personalizzate per un paragrafo o uno stile.
type: docs
weight: 6210
url: /it/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Una raccolta di[`TabStop`](../tabstop/) oggetti che rappresentano schede personalizzate per un paragrafo o uno stile.

Per saperne di più, visita il[Modello oggetto documento Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Ottiene il numero di tabulazioni nella raccolta. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Ottiene un punto di tabulazione all'indice specificato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(TabStop) | Aggiunge o sostituisce un punto di tabulazione nella raccolta. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(double, TabAlignment, TabLeader) | Aggiunge o sostituisce un punto di tabulazione nella raccolta. |
| [After](../../aspose.words/tabstopcollection/after/)(double) | Ottiene una prima tabulazione a destra della posizione specificata. |
| [Before](../../aspose.words/tabstopcollection/before/)(double) | Ottiene una prima tabulazione a sinistra della posizione specificata. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Elimina tutte le posizioni di tabulazione. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(object) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(TabStopCollection) | Determina se specificato`TabStopCollection` ha lo stesso valore della corrente`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Serve come funzione hash per questo tipo. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(double) | Ottiene l'indice di una tabulazione con la posizione specificata in punti. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(int) | Ottiene la posizione (in punti) del punto di tabulazione in corrispondenza dell'indice specificato. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(int) | Rimuove dalla raccolta un punto di tabulazione in corrispondenza dell'indice specificato. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(double) | Rimuove un punto di tabulazione nella posizione specificata dalla raccolta. |

### Osservazioni

Nei documenti di Microsoft Word, una tabulazione può essere definita nelle proprietà di uno stile paragrafo o direttamente nelle proprietà di un paragrafo. Uno stile può essere basato su un altro stile. Pertanto, il set completo di tabulazioni per un dato oggetto è una combinazione di tabulazioni definite direttamente su questo oggetto e tabulazioni ereditate dagli stili principali.

In Aspose.Words, quando ottieni a`TabStopCollection`per un paragrafo o uno stile, contiene solo i punti di tabulazione personalizzati definiti direttamente per questo paragrafo o stile. La raccolta non include i punti di tabulazione definiti negli stili principali o i punti di tabulazione predefiniti.

### Esempi

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 punti corrispondono a un "pollice" sul righello delle tabulazioni di Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Ogni carattere "tab" porta il cursore del builder nella posizione del punto di tabulazione successivo.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Ogni paragrafo ottiene la propria raccolta di tabulazioni, che ne clona i valori dalla raccolta di tabulazioni del generatore di documenti.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Una raccolta di tabulazioni può indirizzarci a TabStop prima e dopo determinate posizioni.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Possiamo cancellare la raccolta di tabulazioni di un paragrafo per ripristinare il comportamento di tabulazione predefinito.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Guarda anche

* class [InternableComplexAttr](../internablecomplexattr/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


