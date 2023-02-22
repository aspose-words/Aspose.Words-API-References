---
title: LayoutCollector.GetStartPageIndex
second_title: Aspose.Words per .NET API Reference
description: LayoutCollector metodo. Ottiene lindice in base 1 della pagina in cui inizia il nodo. Restituisce 0 se il nodo non può essere mappato su una pagina.
type: docs
weight: 70
url: /it/net/aspose.words.layout/layoutcollector/getstartpageindex/
---
## LayoutCollector.GetStartPageIndex method

Ottiene l'indice in base 1 della pagina in cui inizia il nodo. Restituisce 0 se il nodo non può essere mappato su una pagina.

```csharp
public int GetStartPageIndex(Node node)
```

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* spazio dei nomi [Aspose.Words.Layout](../../layoutcollector/)
* assemblea [Aspose.Words](../../../)


