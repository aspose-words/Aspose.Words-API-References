---
title: LayoutCollector.GetEntity
second_title: Aspose.Words per .NET API Reference
description: LayoutCollector metodo. Restituisce una posizione opaca delLayoutEnumerator che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomentoCurrent dato che il documento in corso enumerato e il documento del nodo sono gli stessi.
type: docs
weight: 50
url: /it/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Restituisce una posizione opaca del[`LayoutEnumerator`](../../layoutenumerator/) che corrisponde al nodo specificato. È possibile utilizzare il valore restituito come argomento[`Current`](../../layoutenumerator/current/) dato che il documento in corso enumerato e il documento del nodo sono gli stessi.

```csharp
public object GetEntity(Node node)
```

### Osservazioni

Questo metodo funziona solo per[`Paragraph`](../../../aspose.words/paragraph/) nodi, così come nodi inline indivisibili, ad es[`BookmarkStart`](../../../aspose.words/bookmarkstart/) O[`Shape`](../../../aspose.words.drawing/shape/) . Non funziona per[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) O[`Table`](../../../aspose.words.tables/table/) nodi e nodi all'interno di intestazione/piè di pagina.

Tieni presente che l'entità è stata restituita per a[`Paragraph`](../../../aspose.words/paragraph/) il nodo è un intervallo di interruzione di paragrafo. Utilizzare il metodo appropriato per salire alla linea madre

Se è necessario accedere a a[`Run`](../../../aspose.words/run/) di testo, puoi inserire il segnalibro subito prima di it e quindi passare al segnalibro.

Se è necessario accedere a a[`Cell`](../../../aspose.words.tables/cell/) nodo quindi puoi spostarti su a[`Paragraph`](../../../aspose.words/paragraph/) nodo in questa cella e quindi ascendere a un'entità principale. Lo stesso approccio può essere utilizzato per[`Row`](../../../aspose.words.tables/row/) e[`Table`](../../../aspose.words.tables/table/) nodi.

### Esempi

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* spazio dei nomi [Aspose.Words.Layout](../../layoutcollector/)
* assemblea [Aspose.Words](../../../)


