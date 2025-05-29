---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.NodeCollection, Ihre Lösung für die effiziente Verwaltung verschiedener Knotentypen in der Dokumentenverarbeitung. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 4890
url: /de/net/aspose.words/nodecollection/
---
## NodeCollection class

Stellt eine Sammlung von Knoten eines bestimmten Typs dar.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Ruft einen Knoten am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bestimmt, ob ein Knoten in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Fügt einen Knoten am angegebenen Index in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Kopiert alle Knoten aus der Sammlung in ein neues Knoten-Array. |

## Bemerkungen

`NodeCollection` besitzt nicht die darin enthaltenen Knoten, sondern ist lediglich eine Auswahl von Knoten des angegebenen Typs, aber die Knoten werden im Baum unter ihren jeweiligen übergeordneten Knoten gespeichert.

`NodeCollection` unterstützt indizierten Zugriff, Iteration und bietet Methoden zum Hinzufügen und Entfernen.

Der`NodeCollection` Die Sammlung ist "live", d. h. Änderungen an den untergeordneten Elementen des Knotens object , aus dem sie erstellt wurde, werden sofort in den von der`NodeCollection` Eigenschaften und Methoden.

`NodeCollection` wird zurückgegeben von[`GetChildNodes`](../compositenode/getchildnodes/) und dient auch als Basisklasse für typisierte Knotensammlungen wie[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) usw.

`NodeCollection`kann „flach“ sein und nur unmittelbare untergeordnete Elemente des Knotens enthalten, aus dem es erstellt wurde , oder es kann „tief“ sein und alle untergeordneten Elemente enthalten.

## Beispiele

Zeigt, wie alle Textfeldformen durch Bildformen ersetzt werden.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Siehe auch

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
