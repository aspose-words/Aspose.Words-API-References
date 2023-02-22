---
title: LayoutCollector.LayoutCollector
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutCollector constructeur. Initialisiert eine Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.layout/layoutcollector/layoutcollector/
---
## LayoutCollector constructor

Initialisiert eine Instanz dieser Klasse.

```csharp
public LayoutCollector(Document doc)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | Document | Das Dokument, an das diese Kollektorinstanz angehängt wird. |

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

* class [Document](../../../aspose.words/document/)
* class [LayoutCollector](../)
* namensraum [Aspose.Words.Layout](../../layoutcollector/)
* Montage [Aspose.Words](../../../)


