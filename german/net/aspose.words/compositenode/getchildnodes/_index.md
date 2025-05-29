---
title: CompositeNode.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompositeNode GetChildNodes-Methode – rufen Sie mühelos eine Live-Sammlung von untergeordneten Knoten ab, die auf Ihren angegebenen Typ zugeschnitten sind, um die Leistung zu verbessern.
type: docs
weight: 110
url: /de/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | NodeType | Gibt den Typ der auszuwählenden Knoten an. |
| isDeep | Boolean | `WAHR` um rekursiv aus allen untergeordneten Knoten auszuwählen; `FALSCH` um nur unter unmittelbaren Kindern auszuwählen. |

### Rückgabewert

Eine Live-Sammlung von untergeordneten Knoten des angegebenen Typs.

## Bemerkungen

Die von dieser Methode zurückgegebene Knotensammlung ist immer aktiv.

Eine Live-Sammlung ist immer mit dem Dokument synchronisiert. Wenn Sie beispielsweise alle Abschnitte in einem Dokument auswählen und die Sammlung durchlaufen und dabei die Abschnitte löschen, wird der Abschnitt sofort aus der Sammlung entfernt, wenn er aus dem Dokument entfernt wird.

## Beispiele

Zeigt, wie alle Kommentare und Antworten eines Dokuments gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// Wenn ein Kommentar keinen Vorgänger hat, handelt es sich um einen Kommentar der obersten Ebene und nicht um einen Kommentar vom Typ „Antwort“.
// Alle Kommentare der obersten Ebene zusammen mit allen möglichen Antworten ausdrucken.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Sammlung von Formen aus dem Dokument,
// und speichere die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
            // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die „CustomNodeId“ nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durchlaufen Sie die Sammlung der unmittelbar untergeordneten Elemente des Absatzes.
// und drucke alle Läufe oder Formen aus, die wir darin finden.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

Zeigt, wie untergeordnete Knoten in der Sammlung untergeordneter Knoten eines CompositeNode hinzugefügt, aktualisiert und gelöscht werden.

```csharp
Document doc = new Document();

// Ein leeres Dokument hat standardmäßig einen Absatz.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Zusammengesetzte Knoten wie unser Absatz können andere zusammengesetzte und Inline-Knoten als untergeordnete Elemente enthalten.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Erstellen Sie drei weitere Run-Knoten.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Der Dokumenttext zeigt diese Läufe erst an, wenn wir sie in einen zusammengesetzten Knoten einfügen
// das selbst ein Teil des Knotenbaums des Dokuments ist, wie wir es beim ersten Durchlauf getan haben.
// Wir können bestimmen, wo der Textinhalt der Knoten, die wir einfügen
// erscheint im Dokument, indem eine Einfügeposition relativ zu einem anderen Knoten im Absatz angegeben wird.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Fügen Sie den zweiten Lauf in den Absatz vor dem ersten Lauf ein.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Fügen Sie den dritten Lauf nach dem ersten Lauf ein.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Fügen Sie den ersten Lauf am Anfang der untergeordneten Knotensammlung des Absatzes ein.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Wir können den Inhalt des Laufs ändern, indem wir vorhandene untergeordnete Knoten bearbeiten und löschen.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Siehe auch

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
