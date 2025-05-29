---
title: TabStopCollection Class
linktitle: TabStopCollection
articleTitle: TabStopCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.TabStopCollection. Gestisci facilmente tabulazioni personalizzate per paragrafi e stili, migliorando la formattazione dei tuoi documenti con precisione.
type: docs
weight: 7060
url: /it/net/aspose.words/tabstopcollection/
---
## TabStopCollection class

Una raccolta di[`TabStop`](../tabstop/) oggetti che rappresentano schede personalizzate per un paragrafo o uno stile.

Per saperne di più, visita il[Modello a oggetti del documento (DOM) di Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class TabStopCollection : InternableComplexAttr
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/tabstopcollection/count/) { get; } | Ottiene il numero di tabulazioni nella raccolta. |
| [Item](../../aspose.words/tabstopcollection/item/) { get; } | Ottiene una tabulazione all'indice specificato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/tabstopcollection/add/#add)(*[TabStop](../tabstop/)*) | Aggiunge o sostituisce una tabulazione nella raccolta. |
| [Add](../../aspose.words/tabstopcollection/add/#add_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Aggiunge o sostituisce una tabulazione nella raccolta. |
| [After](../../aspose.words/tabstopcollection/after/)(*double*) | Ottiene una prima tabulazione a destra della posizione specificata. |
| [Before](../../aspose.words/tabstopcollection/before/)(*double*) | Ottiene una prima tabulazione a sinistra della posizione specificata. |
| [Clear](../../aspose.words/tabstopcollection/clear/)() | Elimina tutte le posizioni di tabulazione. |
| override [Equals](../../aspose.words/tabstopcollection/equals/#equals_1)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| [Equals](../../aspose.words/tabstopcollection/equals/#equals)(*TabStopCollection*) | Determina se il valore specificato`TabStopCollection` ha un valore uguale a quello attuale`TabStopCollection` . |
| override [GetHashCode](../../aspose.words/tabstopcollection/gethashcode/)() | Serve come funzione hash per questo tipo. |
| [GetIndexByPosition](../../aspose.words/tabstopcollection/getindexbyposition/)(*double*) | Ottiene l'indice di una tabulazione con la posizione specificata in punti. |
| [GetPositionByIndex](../../aspose.words/tabstopcollection/getpositionbyindex/)(*int*) | Ottiene la posizione (in punti) della tabulazione all'indice specificato. |
| [RemoveByIndex](../../aspose.words/tabstopcollection/removebyindex/)(*int*) | Rimuove una tabulazione all'indice specificato dalla raccolta. |
| [RemoveByPosition](../../aspose.words/tabstopcollection/removebyposition/)(*double*) | Rimuove una tabulazione nella posizione specificata dalla raccolta. |

## Osservazioni

Nei documenti di Microsoft Word, una tabulazione può essere definita nelle proprietà di uno stile di paragrafo o direttamente nelle proprietà di un paragrafo. Uno stile può essere basato su un altro stile. Pertanto, l'insieme completo di tabulazioni per un dato oggetto è una combinazione di tabulazioni definite direttamente su questo oggetto e tabulazioni ereditate dagli stili padre.

In Aspose.Words, quando si ottiene un`TabStopCollection` per un paragrafo o uno stile, contiene solo le tabulazioni personalizzate definite direttamente per questo paragrafo o stile. La raccolta non include le tabulazioni definite negli stili padre o le tabulazioni predefinite.

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

* class [InternableComplexAttr](../internablecomplexattr/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
