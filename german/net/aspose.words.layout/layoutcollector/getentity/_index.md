---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetEntity-Methode des LayoutCollector und rufen Sie mühelos die Position des LayoutEnumerators ab, um eine nahtlose Dokumentnavigation und verbesserte Produktivität zu ermöglichen.
type: docs
weight: 50
url: /de/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Gibt eine undurchsichtige Position des[`LayoutEnumerator`](../../layoutenumerator/) der dem angegebenen Knoten entspricht. Sie können den zurückgegebenen Wert als Argument verwenden, um[`Current`](../../layoutenumerator/current/) vorausgesetzt, das aufzuzählende Dokument und das Dokument des Knotens sind identisch.

```csharp
public object GetEntity(Node node)
```

## Bemerkungen

Diese Methode funktioniert nur für[`Paragraph`](../../../aspose.words/paragraph/) Knoten, sowie unteilbare Inline-Knoten, zB[`BookmarkStart`](../../../aspose.words/bookmarkstart/) oder[`Shape`](../../../aspose.words.drawing/shape/) Es funktioniert nicht für[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) oder[`Table`](../../../aspose.words.tables/table/) Knoten und Knoten innerhalb der Kopf-/Fußzeile.

Beachten Sie, dass die Entität für eine[`Paragraph`](../../../aspose.words/paragraph/)Knoten ist ein Absatzumbruch. Verwenden Sie die entsprechende Methode, um zur übergeordneten Zeile aufzusteigen

Wenn Sie zu einem[`Run`](../../../aspose.words/run/) von Text, dann können Sie direkt davor ein Lesezeichen einfügen und dann stattdessen zum Lesezeichen navigieren.

Wenn Sie zu einem[`Cell`](../../../aspose.words.tables/cell/) Knoten, dann können Sie zu einem[`Paragraph`](../../../aspose.words/paragraph/) Knoten in dieser Zelle und steigen dann zu einer übergeordneten Entität auf. Der gleiche Ansatz kann verwendet werden für[`Row`](../../../aspose.words.tables/row/) und[`Table`](../../../aspose.words.tables/table/) Knoten.

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

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
