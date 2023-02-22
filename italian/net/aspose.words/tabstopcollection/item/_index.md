---
title: TabStopCollection.Item
second_title: Aspose.Words per .NET API Reference
description: TabStopCollection proprietà. Ottiene un punto di tabulazione in corrispondenza dellindice specificato.
type: docs
weight: 20
url: /it/net/aspose.words/tabstopcollection/item/
---
## TabStopCollection indexer (1 of 2)

Ottiene un punto di tabulazione in corrispondenza dell'indice specificato.

```csharp
public TabStop this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nella raccolta di tabulazioni. |

### Esempi

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 punti sono un "pollice" sul righello di interruzione di tabulazione di Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Ogni carattere "tab" porta il cursore del builder nella posizione del successivo punto di tabulazione.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Ogni paragrafo ottiene la sua raccolta di tabulazioni, che clona i suoi valori dalla raccolta di tabulazioni del generatore di documenti.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Una raccolta di tabulazioni può indicarci TabStop prima e dopo determinate posizioni.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Possiamo cancellare la raccolta di tabulazioni di un paragrafo per ripristinare il comportamento di tabulazione predefinito.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Guarda anche

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../tabstopcollection/)
* assemblea [Aspose.Words](../../../)

---

## TabStopCollection indexer (2 of 2)

Ottiene un punto di tabulazione nella posizione specificata.

```csharp
public TabStop this[double position] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| position | La posizione (in punti) del punto di tabulazione. |

### Osservazioni

Restituisce null se non viene trovato alcun punto di tabulazione nella posizione specificata.

### Esempi

Mostra come lavorare con la raccolta di tabulazioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 punti sono un "pollice" sul righello di interruzione di tabulazione di Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Ogni carattere "tab" porta il cursore del builder nella posizione del successivo punto di tabulazione.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Ogni paragrafo ottiene la sua raccolta di tabulazioni, che clona i suoi valori dalla raccolta di tabulazioni del generatore di documenti.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Una raccolta di tabulazioni può indicarci TabStop prima e dopo determinate posizioni.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Possiamo cancellare la raccolta di tabulazioni di un paragrafo per ripristinare il comportamento di tabulazione predefinito.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Guarda anche

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* spazio dei nomi [Aspose.Words](../../tabstopcollection/)
* assemblea [Aspose.Words](../../../)


