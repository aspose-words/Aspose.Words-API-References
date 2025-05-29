---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos alle Formen aus Ihrem Text mit der DeleteShapes-Methode. Vereinfachen Sie Ihren Inhalt und verbessern Sie die Übersichtlichkeit!
type: docs
weight: 70
url: /de/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Löscht alle Formen aus dem Text dieser Geschichte.

```csharp
public void DeleteShapes()
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

* class [Story](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
