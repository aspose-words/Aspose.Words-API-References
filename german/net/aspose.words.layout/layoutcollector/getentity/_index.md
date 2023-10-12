---
title: LayoutCollector.GetEntity
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutCollector methode. Gibt eine undurchsichtige Position des zurückLayoutEnumerator was dem angegebenen Knoten entspricht. Sie können den zurückgegebenen Wert als Argument für verwendenCurrent vorausgesetzt dass das Dokument das aufgezählt wird und das Dokument des Knotens gleich sind.
type: docs
weight: 50
url: /de/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Gibt eine undurchsichtige Position des zurück[`LayoutEnumerator`](../../layoutenumerator/) was dem angegebenen Knoten entspricht. Sie können den zurückgegebenen Wert als Argument für verwenden[`Current`](../../layoutenumerator/current/) vorausgesetzt, dass das Dokument, das aufgezählt wird, und das Dokument des Knotens gleich sind.

```csharp
public object GetEntity(Node node)
```

### Bemerkungen

Diese Methode funktioniert nur für[`Paragraph`](../../../aspose.words/paragraph/) Knoten sowie unteilbare Inline-Knoten, zB[`BookmarkStart`](../../../aspose.words/bookmarkstart/) oder[`Shape`](../../../aspose.words.drawing/shape/) . Es funktioniert nicht[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) oder[`Table`](../../../aspose.words.tables/table/) Knoten und Knoten innerhalb der Kopf-/Fußzeile.

Beachten Sie, dass die Entität für a zurückgegeben wurde[`Paragraph`](../../../aspose.words/paragraph/) Knoten ist ein Absatzumbruchbereich. Verwenden Sie die entsprechende Methode, um zur übergeordneten Linie aufzusteigen

Wenn Sie zu a navigieren müssen[`Run`](../../../aspose.words/run/) Wenn Sie einen Text haben, können Sie direkt vor it ein Lesezeichen einfügen und dann stattdessen zum Lesezeichen navigieren.

Wenn Sie zu a navigieren müssen[`Cell`](../../../aspose.words.tables/cell/) Knoten, dann können Sie zu einem wechseln[`Paragraph`](../../../aspose.words/paragraph/) -Knoten in dieser Zelle und steigen Sie dann zu einer übergeordneten Entität auf. Der gleiche Ansatz kann verwendet werden für[`Row`](../../../aspose.words.tables/row/) und[`Table`](../../../aspose.words.tables/table/) Knoten.

### Beispiele

Zeigt, wie die Seitenbereiche angezeigt werden, die ein Knoten umfasst.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Rufen Sie die Methode „GetNumPagesSpanned“ auf, um zu zählen, wie viele Seiten der Inhalt unseres Dokuments umfasst.
// Da das Dokument leer ist, beträgt die Anzahl der Seiten derzeit Null.
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

// Vor dem Layout-Kollektor müssen wir die Methode „UpdatePageLayout“ aufrufen, um sie uns zu geben
// eine genaue Zahl für alle Layout-bezogenen Metriken, wie zum Beispiel die Seitenzahl.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Wir können die Nummern der Start- und Endseiten jedes Knotens und deren gesamte Seitenspanne sehen.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Wir können die Layout-Entitäten mit einem LayoutEnumerator durchlaufen.
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
* namensraum [Aspose.Words.Layout](../../layoutcollector/)
* Montage [Aspose.Words](../../../)


