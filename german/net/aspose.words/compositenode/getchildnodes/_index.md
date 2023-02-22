---
title: CompositeNode.GetChildNodes
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode methode. Gibt eine LiveSammlung von untergeordneten Knoten zurück die dem angegebenen Typ entsprechen.
type: docs
weight: 100
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
| isDeep | Boolean | True, um rekursiv aus allen untergeordneten Knoten auszuwählen. False, um nur unter unmittelbar untergeordneten Knoten auszuwählen. |

### Rückgabewert

Eine Live-Sammlung von untergeordneten Knoten des angegebenen Typs.

### Bemerkungen

Die von dieser Methode zurückgegebene Sammlung von Knoten ist immer aktiv.

Eine Live-Sammlung ist immer mit dem Dokument synchron. Wenn Sie beispielsweise alle Abschnitte in einem Dokument ausgewählt haben und durch die Sammlung aufzählen und die Abschnitte löschen, wird der Abschnitt sofort aus der Sammlung entfernt , wenn er aus dem Dokument entfernt wird.

### Beispiele

Zeigt, wie alle Kommentare eines Dokuments und ihre Antworten gedruckt werden.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// Wenn ein Kommentar keinen Vorfahren hat, handelt es sich um einen "Top-Level"-Kommentar im Gegensatz zu einem Antworttyp-Kommentar.
// Drucken Sie alle Kommentare der obersten Ebene zusammen mit allen möglichen Antworten.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
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
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
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

Zeigt, wie untergeordnete Knoten in der Sammlung untergeordneter Elemente eines CompositeNode hinzugefügt, aktualisiert und gelöscht werden.

```csharp
Document doc = new Document();

// Ein leeres Dokument hat standardmäßig einen Absatz.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Zusammengesetzte Knoten wie unser Absatz können andere zusammengesetzte und Inline-Knoten als Kinder enthalten.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Drei weitere Ausführungsknoten erstellen.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Der Dokumentkörper zeigt diese Läufe erst an, wenn wir sie in einen zusammengesetzten Knoten einfügen
// das selbst ein Teil des Knotenbaums des Dokuments ist, wie wir es beim ersten Durchlauf getan haben.
// Wir können bestimmen, wo sich der Textinhalt von Knoten befindet, die wir einfügen
// wird im Dokument angezeigt, indem eine Einfügeposition relativ zu einem anderen Knoten im Absatz angegeben wird.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Füge den zweiten Lauf in den Absatz vor dem ersten Lauf ein.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Füge den dritten Lauf nach dem ersten Lauf ein.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Den ersten Lauf am Anfang der Sammlung untergeordneter Knoten des Absatzes einfügen.
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
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


