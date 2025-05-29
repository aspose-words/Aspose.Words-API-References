---
title: LayoutCollector.GetEndPageIndex
linktitle: GetEndPageIndex
articleTitle: GetEndPageIndex
second_title: Aspose.Words per .NET
description: Scopri il metodo GetEndPageIndex di LayoutCollector per trovare facilmente l'indice a partire da 1 della pagina finale di un nodo. Semplifica la mappatura delle tue pagine oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.layout/layoutcollector/getendpageindex/
---
## LayoutCollector.GetEndPageIndex method

Ottiene l'indice a partire da 1 della pagina in cui termina il nodo. Restituisce 0 se il nodo non può essere mappato a una pagina.

```csharp
public int GetEndPageIndex(Node node)
```

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
