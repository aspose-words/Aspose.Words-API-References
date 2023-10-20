---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.LayoutCollector klas. Mit dieser Klasse können Seitenzahlen von Dokumentknoten berechnet werden in C#.
type: docs
weight: 3320
url: /de/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Mit dieser Klasse können Seitenzahlen von Dokumentknoten berechnet werden.

Um mehr zu erfahren, besuchen Sie die[Konvertieren in das Fixed-Page-Format](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) Dokumentationsartikel.

```csharp
public class LayoutCollector
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Ruft das Dokument ab, an das diese Collector-Instanz angehängt ist, oder legt dieses fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Löscht alle gesammelten Layoutdaten. Rufen Sie diese Methode auf, nachdem das Dokument manuell aktualisiert oder das Layout neu erstellt wurde. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Ruft den 1-basierten Index der Seite ab, auf der der Knoten endet. Gibt 0 zurück, wenn der Knoten keiner Seite zugeordnet werden kann. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Gibt eine undurchsichtige Position des zurück[`LayoutEnumerator`](../layoutenumerator/) was dem angegebenen Knoten entspricht. Sie können den zurückgegebenen Wert als Argument für verwenden[`Current`](../layoutenumerator/current/) vorausgesetzt, dass das Dokument, das aufgezählt wird, und das Dokument des Knotens gleich sind. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Ruft die Anzahl der Seiten ab, die der angegebene Knoten umfasst. 0, wenn sich der Knoten innerhalb einer einzelnen Seite befindet. Dies ist dasselbe wie[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Ruft den 1-basierten Index der Seite ab, auf der der Knoten beginnt. Gibt 0 zurück, wenn der Knoten keiner Seite zugeordnet werden kann. |

## Bemerkungen

Wenn Sie eine erstellen`LayoutCollector` und geben Sie a an[`Document`](../../aspose.words/document/) Dokumentobjekt, an das angehängt werden soll. Der Collector zeichnet die Zuordnung von Dokumentknoten zu Layoutobjekten auf, wenn das Dokument in Seiten formatiert wird.

Mit dem können Sie herausfinden, auf welcher Seite sich ein bestimmter Dokumentknoten (z. B. Lauf, Absatz oder Tabellenzelle) befindet [`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) Und[`GetNumPagesSpanned`](./getnumpagesspanned/)Methoden. Diese Methoden erstellen automatisch ein Seitenlayoutmodell des Dokuments und aktualisieren Felder bei Bedarf.

Wenn Sie keine Layoutinformationen mehr sammeln müssen, legen Sie am besten die fest[`Document`](./document/) Eigentum zu`Null` , um eine unnötige Sammlung weiterer Layoutzuordnungen zu vermeiden.

## Beispiele

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
