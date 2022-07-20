---
title: GetNumPagesSpanned
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft die Anzahl der Seiten ab die der angegebene Knoten umfasst. 0 wenn sich der Knoten innerhalb einer einzelnen Seite befindet. Dies ist dasselbe wieGetEndPageIndexaspose.words.layout/layoutcollector/getendpageindex -GetStartPageIndexaspose.words.layout/layoutcollector/getstartpageindex .
type: docs
weight: 60
url: /de/net/aspose.words.layout/layoutcollector/getnumpagesspanned/
---
## LayoutCollector.GetNumPagesSpanned method

Ruft die Anzahl der Seiten ab, die der angegebene Knoten umfasst. 0, wenn sich der Knoten innerhalb einer einzelnen Seite befindet. Dies ist dasselbe wie[`GetEndPageIndex`](../getendpageindex) -[`GetStartPageIndex`](../getstartpageindex) .

```csharp
public int GetNumPagesSpanned(Node node)
```

### Beispiele

Zeigt, wie die Seitenbereiche angezeigt werden, die ein Knoten umfasst.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Rufen Sie die Methode "GetNumPagesSpanned" auf, um zu zählen, wie viele Seiten der Inhalt unseres Dokuments umfasst.
// Da das Dokument leer ist, ist diese Seitenzahl derzeit null.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Das Dokument mit 5 Seiten Inhalt füllen.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Vor dem Layout-Sammler müssen wir die Methode "UpdatePageLayout" aufrufen, um uns zu geben
// eine genaue Zahl für alle Layout-bezogenen Metriken, wie z. B. die Seitenzahl.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Wir können die Nummern der Start- und Endseiten jedes Knotens und ihre gesamten Seitenspannen sehen.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Wir können mit einem LayoutEnumerator über die Layout-Entitäten iterieren.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// Der LayoutEnumerator kann die Sammlung von Layout-Entitäten wie einen Baum durchlaufen.
// Wir können es auch auf die entsprechende Layout-Entität eines beliebigen Knotens anwenden.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Siehe auch

* class [Node](../../../aspose.words/node)
* class [LayoutCollector](../../layoutcollector)
* namensraum [Aspose.Words.Layout](../../layoutcollector)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->