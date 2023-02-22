---
title: CompositeNode.IndexOf
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode methode. Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück.
type: docs
weight: 130
url: /de/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück.

```csharp
public int IndexOf(Node child)
```

### Bemerkungen

Gibt -1 zurück, wenn der Knoten nicht in den untergeordneten Knoten gefunden wird.

### Beispiele

Zeigt, wie der Index eines bestimmten untergeordneten Knotens von seinem übergeordneten Knoten abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Den Index des letzten Absatzes im Hauptteil des ersten Abschnitts abrufen.
Assert.AreEqual(24, body.ChildNodes.IndexOf(body.LastParagraph));
```

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


