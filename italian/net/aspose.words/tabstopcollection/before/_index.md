---
title: Before
second_title: Aspose.Words per .NET API Reference
description: Ottiene una prima tabulazione a sinistra della posizione specificata.
type: docs
weight: 50
url: /it/net/aspose.words/tabstopcollection/before/
---
## TabStopCollection.Before method

Ottiene una prima tabulazione a sinistra della posizione specificata.

```csharp
public TabStop Before(double position)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| position | Double | La posizione di riferimento (in punti). |

### Valore di ritorno

Un oggetto punto di tabulazione o null se non è stato trovato un punto di tabulazione adatto.

### Osservazioni

Salta le tabulazioni con **Allineamento** impostato`TabAlignment.Bar`.

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

* class [TabStop](../../tabstop)
* class [TabStopCollection](../../tabstopcollection)
* spazio dei nomi [Aspose.Words](../../tabstopcollection)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->