---
title: Document.EnsureMinimum
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Wenn das Dokument keine Abschnitte enthält wird ein Abschnitt mit einem Absatz erstellt.
type: docs
weight: 600
url: /de/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt.

```csharp
public void EnsureMinimum()
```

### Beispiele

Zeigt, wie sichergestellt wird, dass ein Dokument die minimale Menge an Knoten enthält, die zum Bearbeiten seines Inhalts erforderlich sind.

```csharp
// Ein neu erstelltes Dokument enthält einen untergeordneten Abschnitt, der einen untergeordneten Textkörper und einen untergeordneten Absatz enthält.
// Wir können den Inhalt des Dokumentkörpers bearbeiten, indem wir diesem Absatz Knoten wie Runs oder Inline-Shapes hinzufügen.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Dies ist die minimale Menge an Knoten, die wir benötigen, um das Dokument bearbeiten zu können.
// Wir können das Dokument nicht mehr bearbeiten, wenn wir eines davon entfernen.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Rufen Sie diese Methode auf, um sicherzustellen, dass das Dokument mindestens diese drei Knoten hat, damit wir es erneut bearbeiten können.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


