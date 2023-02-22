---
title: Class LayoutCollector
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Layout.LayoutCollector classe. Questa classe consente di calcolare i numeri di pagina dei nodi del documento.
type: docs
weight: 3120
url: /it/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Questa classe consente di calcolare i numeri di pagina dei nodi del documento.

```csharp
public class LayoutCollector
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | Inizializza un'istanza di questa classe. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Ottiene o imposta il documento a cui è allegata questa istanza di raccolta. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Cancella tutti i dati di layout raccolti. Chiama questo metodo dopo che il documento è stato aggiornato manualmente o il layout è stato ricostruito. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Ottiene l'indice in base 1 della pagina in cui termina il nodo. Restituisce 0 se il nodo non può essere mappato su una pagina. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | Restituisce una posizione opaca di[`LayoutEnumerator`](../layoutenumerator/) che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomento per[`Current`](../layoutenumerator/current/) dato che il documento viene enumerato e il documento del nodo sono gli stessi. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Ottiene il numero di pagine su cui si estende il nodo specificato. 0 se il nodo è all'interno di una singola pagina. È lo stesso di[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Ottiene l'indice in base 1 della pagina in cui inizia il nodo. Restituisce 0 se il nodo non può essere mappato su una pagina. |

### Osservazioni

Quando crei un`LayoutCollector` e specificare a[`Document`](../../aspose.words/document/)oggetto del documento a cui allegare, il raccoglitore registrerà la mappatura dei nodi del documento agli oggetti del layout quando il documento viene formattato in pagine.

Sarai in grado di scoprire su quale pagina si trova un particolare nodo del documento (ad es. esecuzione, paragrafo o cella di tabella) utilizzando il[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) e[`GetNumPagesSpanned`](./getnumpagesspanned/) metodi. Questi metodi creano automaticamente il modello di layout di pagina del documento e aggiornano i campi se necessario.

Quando non è più necessario raccogliere informazioni sul layout, è meglio impostare il[`Document`](./document/) proprietà su null per evitare la raccolta non necessaria di più mappature di layout.

### Esempi

Mostra come visualizzare gli intervalli di pagine su cui si estende un nodo.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Chiama il metodo "GetNumPagesSpanned" per contare quante pagine si estende il contenuto del nostro documento.
// Poiché il documento è vuoto, il numero di pagine attualmente è zero.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Popolare il documento con 5 pagine di contenuto.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Prima del raccoglitore di layout, dobbiamo chiamare il metodo "UpdatePageLayout" per fornirci
// una cifra precisa per qualsiasi metrica relativa al layout, come il conteggio delle pagine.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Possiamo vedere i numeri delle pagine iniziali e finali di qualsiasi nodo e le loro estensioni di pagina complessive.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Possiamo scorrere le entità del layout usando un LayoutEnumerator.
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


