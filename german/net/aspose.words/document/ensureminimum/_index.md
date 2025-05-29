---
title: Document.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie mit der Methode EnsureMinimum automatisch Abschnitte und Absätze in Dokumenten erstellen und so vollständige und organisierte Inhalte sicherstellen.
type: docs
weight: 620
url: /de/net/aspose.words/document/ensureminimum/
---
## Document.EnsureMinimum method

Wenn das Dokument keine Abschnitte enthält, wird ein Abschnitt mit einem Absatz erstellt.

```csharp
public void EnsureMinimum()
```

## Beispiele

Zeigt, wie sichergestellt wird, dass ein Dokument den zum Bearbeiten seines Inhalts erforderlichen Mindestsatz an Knoten enthält.

```csharp
// Ein neu erstelltes Dokument enthält einen untergeordneten Abschnitt, der wiederum einen untergeordneten Textkörper und einen untergeordneten Absatz enthält.
// Wir können den Inhalt des Dokumenttexts bearbeiten, indem wir diesem Absatz Knoten wie Läufe oder Inline-Formen hinzufügen.
Document doc = new Document();
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(doc, nodes[0].ParentNode);

Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(nodes[0], nodes[1].ParentNode);

Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);
Assert.AreEqual(nodes[1], nodes[2].ParentNode);

// Dies ist der minimale Satz an Knoten, den wir benötigen, um das Dokument bearbeiten zu können.
// Wenn wir eines davon entfernen, können wir das Dokument nicht mehr bearbeiten.
doc.RemoveAllChildren();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);

// Rufen Sie diese Methode auf, um sicherzustellen, dass das Dokument mindestens diese drei Knoten enthält, damit wir es erneut bearbeiten können.
doc.EnsureMinimum();

Assert.AreEqual(NodeType.Section, nodes[0].NodeType);
Assert.AreEqual(NodeType.Body, nodes[1].NodeType);
Assert.AreEqual(NodeType.Paragraph, nodes[2].NodeType);

((Paragraph)nodes[2]).Runs.Add(new Run(doc, "Hello world!"));
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
