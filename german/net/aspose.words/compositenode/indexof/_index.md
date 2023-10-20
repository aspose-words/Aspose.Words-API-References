---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words für .NET
description: CompositeNode IndexOf methode. Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten KnotenArray zurück in C#.
type: docs
weight: 120
url: /de/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück.

```csharp
public int IndexOf(Node child)
```

## Bemerkungen

Gibt -1 zurück, wenn der Knoten nicht in den untergeordneten Knoten gefunden wird.

## Beispiele

Zeigt, wie der Index eines bestimmten untergeordneten Knotens von seinem übergeordneten Knoten abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Den Index des letzten Absatzes im Hauptteil des ersten Abschnitts abrufen.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
