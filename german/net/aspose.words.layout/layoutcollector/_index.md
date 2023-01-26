---
title: LayoutCollector
second_title: Aspose.Words für .NET-API-Referenz
description: Diese Klasse ermöglicht es Seitenzahlen von Dokumentknoten zu berechnen.
type: docs
weight: 3120
url: /de/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Diese Klasse ermöglicht es, Seitenzahlen von Dokumentknoten zu berechnen.

```csharp
public class LayoutCollector
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LayoutCollector](layoutcollector/)(Document) | Initialisiert eine Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Ruft das Dokument ab oder legt es fest, an das diese Collector-Instanz angehängt ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Löscht alle gesammelten Layoutdaten. Rufen Sie diese Methode auf, nachdem das Dokument manuell aktualisiert oder das Layout neu erstellt wurde. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(Node) | Ruft den 1-basierten Index der Seite ab, auf der der Knoten endet. Gibt 0 zurück, wenn der Knoten keiner Seite zugeordnet werden kann. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(Node) | Gibt eine undurchsichtige Position von zurück[`LayoutEnumerator`](../layoutenumerator/) was dem angegebenen Knoten entspricht. Sie können den zurückgegebenen Wert als Argument für verwenden[`Current`](../layoutenumerator/current/) Da das Dokument, das aufgezählt wird, und das Dokument des Knotens identisch sind. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(Node) | Ruft die Anzahl der Seiten ab, die der angegebene Knoten umfasst. 0, wenn sich der Knoten innerhalb einer einzelnen Seite befindet. Dies ist dasselbe wie[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(Node) | Ruft den 1-basierten Index der Seite ab, auf der der Knoten beginnt. Gibt 0 zurück, wenn der Knoten keiner Seite zugeordnet werden kann. |

### Bemerkungen

Beim Erstellen eines`LayoutCollector` und spezifizieren a[`Document`](../../aspose.words/document/)Dokumentobjekt, an das angehängt werden soll, der Kollektor zeichnet die Zuordnung von Dokumentknoten zu Layoutobjekten auf, wenn das Dokument in Seiten formatiert wird.

Auf welcher Seite sich ein bestimmter Dokumentknoten (z. B. Lauf, Absatz oder Tabellenzelle) befindet können Sie mit dem ermitteln[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) und[`GetNumPagesSpanned`](./getnumpagesspanned/) Methoden. Diese Methoden erstellen automatisch ein Seitenlayoutmodell des Dokuments und aktualisieren Felder, falls erforderlich.

Wenn Sie keine Layoutinformationen mehr sammeln müssen, ist es am besten, die[`Document`](./document/) -Eigenschaft auf null , um eine unnötige Erfassung weiterer Layoutzuordnungen zu vermeiden.

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
