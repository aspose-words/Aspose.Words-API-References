---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words per .NET
description: Aspose.Words.Layout.LayoutCollector classe. Questa classe consente di calcolare i numeri di pagina dei nodi del documento in C#.
type: docs
weight: 3320
url: /it/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Questa classe consente di calcolare i numeri di pagina dei nodi del documento.

Per saperne di più, visita il[Conversione nel formato a pagina fissa](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) articolo di documentazione.

```csharp
public class LayoutCollector
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Inizializza un'istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Ottiene o imposta il documento a cui è allegata questa istanza del raccoglitore. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Cancella tutti i dati di layout raccolti. Chiama questo metodo dopo che il documento è stato aggiornato manualmente o il layout è stato ricostruito. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Ottiene l'indice in base 1 della pagina in cui termina il nodo. Restituisce 0 se il nodo non può essere mappato su una pagina. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Restituisce una posizione opaca del[`LayoutEnumerator`](../layoutenumerator/) che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomento[`Current`](../layoutenumerator/current/) dato che il documento in corso enumerato e il documento del nodo sono gli stessi. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Ottiene il numero di pagine su cui si estende il nodo specificato. 0 se il nodo si trova all'interno di una singola pagina. È uguale a[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Ottiene l'indice in base 1 della pagina in cui inizia il nodo. Restituisce 0 se il nodo non può essere mappato su una pagina. |

## Osservazioni

Quando crei un file`LayoutCollector` e specificare a[`Document`](../../aspose.words/document/) oggetto documento a cui allegare, il raccoglitore registrerà la mappatura dei nodi del documento sugli oggetti del layout quando il documento viene formattato in pagine.

Potrai scoprire in quale pagina si trova un particolare nodo del documento (es. sequenza, paragrafo o cella di tabella) utilizzando il comando[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) E[`GetNumPagesSpanned`](./getnumpagesspanned/)metodi. Questi metodi creano automaticamente il modello di layout della pagina del documento e aggiornano i campi, se necessario.

Quando non è più necessario raccogliere informazioni sul layout, è meglio impostare il file[`Document`](./document/) proprietà a`nullo` per evitare la raccolta non necessaria di più mappature di layout.

## Esempi

Mostra come visualizzare gli intervalli di pagine su cui si estende un nodo.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Chiama il metodo "GetNumPagesSpanned" per contare quante pagine si estende il contenuto del nostro documento.
// Poiché il documento è vuoto, il numero di pagine attualmente è zero.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Compila il documento con 5 pagine di contenuto.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Prima del raccoglitore di layout, dobbiamo chiamare il metodo "UpdatePageLayout" per darci
// una cifra precisa per qualsiasi metrica relativa al layout, come il conteggio delle pagine.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Possiamo vedere i numeri delle pagine iniziali e finali di qualsiasi nodo e la loro estensione complessiva delle pagine.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Possiamo scorrere le entità del layout utilizzando un LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator può attraversare la raccolta di entità di layout come un albero.
// Possiamo anche applicarlo all'entità di layout corrispondente di qualsiasi nodo.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
