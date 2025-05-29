---
title: LayoutCollector.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words für .NET
description: Entdecken Sie die Dokumenteigenschaft von LayoutCollector, um Dokumentanhänge einfach zu verwalten und anzupassen und so die Effizienz Ihres Arbeitsablaufs zu steigern.
type: docs
weight: 20
url: /de/net/aspose.words.layout/layoutcollector/document/
---
## LayoutCollector.Document property

Ruft das Dokument ab oder legt es fest, an das diese Collector-Instanz angehängt ist.

```csharp
public Document Document { get; set; }
```

## Bemerkungen

Wenn Sie auf die Seitenindizes der Dokumentknoten zugreifen müssen, müssen Sie diese Eigenschaft so setzen, dass sie auf eine Dokumentinstanz verweist, bevor das Seitenlayout des Dokuments erstellt wird. Am besten setzen Sie diese Eigenschaft auf`null` danach, andernfalls sammelt der Collector weiterhin Informationen aus nachfolgenden Neuerstellungen des Seitenlayouts des Dokuments.

## Beispiele

Zeigt, wie die Seitenbereiche angezeigt werden, die ein Knoten umfasst.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Rufen Sie die Methode „GetNumPagesSpanned“ auf, um zu zählen, wie viele Seiten der Inhalt unseres Dokuments umfasst.
// Da das Dokument leer ist, beträgt die Seitenanzahl derzeit Null.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Füllen Sie das Dokument mit 5 Seiten Inhalt.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Vor dem Layout-Sammler müssen wir die Methode "UpdatePageLayout" aufrufen, um uns
// eine genaue Zahl für jede layoutbezogene Metrik, wie beispielsweise die Seitenanzahl.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Wir können die Nummern der Start- und Endseiten jedes Knotens und ihre Gesamtseitenspanne sehen.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Wir können die Layout-Entitäten mithilfe eines LayoutEnumerators durchlaufen.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// Der LayoutEnumerator kann die Sammlung von Layout-Entitäten wie einen Baum durchlaufen.
// Wir können es auch auf die entsprechende Layout-Entität eines beliebigen Knotens anwenden.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Siehe auch

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
