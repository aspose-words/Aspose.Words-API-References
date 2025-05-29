---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words für .NET
description: Entdecken Sie die StoryType-Eigenschaft, um Ihre Geschichten einfach zu identifizieren und zu kategorisieren, die Organisation zu verbessern und Ihr Storytelling-Erlebnis zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words/story/storytype/
---
## Story.StoryType property

Ruft den Typ dieser Story ab.

```csharp
public StoryType StoryType { get; }
```

## Beispiele

Zeigt, wie alle Formen aus einem Knoten entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen DocumentBuilder, um eine Form einzufügen. Dies ist eine Inline-Form.
// der einen übergeordneten Absatz hat, der ein untergeordneter Knoten des Hauptteils des ersten Abschnitts ist.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Wir können alle Formen aus den untergeordneten Absätzen dieses Textkörpers löschen.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Siehe auch

* enum [StoryType](../../storytype/)
* class [Story](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
