---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEntity di LayoutCollector e recupera senza sforzo la posizione di LayoutEnumerator per una navigazione fluida nei documenti e una maggiore produttività.
type: docs
weight: 50
url: /it/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Restituisce una posizione opaca del[`LayoutEnumerator`](../../layoutenumerator/) che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomento per[`Current`](../../layoutenumerator/current/) dato che il documento che viene enumerato e il documento del nodo sono gli stessi.

```csharp
public object GetEntity(Node node)
```

## Osservazioni

Questo metodo funziona solo per[`Paragraph`](../../../aspose.words/paragraph/) nodi, così come nodi in linea indivisibili, ad esempio[`BookmarkStart`](../../../aspose.words/bookmarkstart/) O[`Shape`](../../../aspose.words.drawing/shape/) Non funziona per[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) O[`Table`](../../../aspose.words.tables/table/) nodi e nodi all'interno dell'intestazione/piè di pagina.

Si noti che l'entità è stata restituita per un[`Paragraph`](../../../aspose.words/paragraph/)Il nodo è un'interruzione di paragrafo. Utilizza il metodo appropriato per risalire alla riga padre.

Se hai bisogno di navigare verso un[`Run`](../../../aspose.words/run/) di testo, puoi inserire un segnalibro subito prima di esso e poi passare al segnalibro.

Se hai bisogno di navigare verso un[`Cell`](../../../aspose.words.tables/cell/) nodo quindi puoi spostarti su un[`Paragraph`](../../../aspose.words/paragraph/) nodo in questa cella e poi ascendere a un'entità padre. Lo stesso approccio può essere utilizzato per[`Row`](../../../aspose.words.tables/row/) e[`Table`](../../../aspose.words.tables/table/) nodi.

## Esempi

Mostra come visualizzare gli intervalli di pagine su cui si estende un nodo.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Chiama il metodo "GetNumPagesSpanned" per contare su quante pagine si estende il contenuto del nostro documento.
// Poiché il documento è vuoto, il numero di pagine è attualmente zero.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Popola il documento con 5 pagine di contenuto.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Prima del layout collector, dobbiamo chiamare il metodo "UpdatePageLayout" per fornirci
// un valore preciso per qualsiasi metrica correlata al layout, come il numero di pagine.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Possiamo vedere i numeri delle pagine iniziali e finali di ogni nodo e la loro estensione complessiva di pagina.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Possiamo scorrere le entità di layout utilizzando un LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator può attraversare la raccolta di entità di layout come un albero.
// Possiamo applicarlo anche a qualsiasi entità layout corrispondente a un nodo.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Guarda anche

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
