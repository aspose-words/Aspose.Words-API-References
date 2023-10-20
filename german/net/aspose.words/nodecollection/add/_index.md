---
title: NodeCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: NodeCollection Add methode. Fügt einen Knoten am Ende der Sammlung hinzu in C#.
type: docs
weight: 30
url: /de/net/aspose.words/nodecollection/add/
---
## NodeCollection.Add method

Fügt einen Knoten am Ende der Sammlung hinzu.

```csharp
public void Add(Node node)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | Node | Der Knoten, der am Ende der Sammlung hinzugefügt werden soll. |

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| NotSupportedException | Der[`NodeCollection`](../) ist eine „tiefe“ Sammlung. |

## Bemerkungen

Der Knoten wird als untergeordnetes Element in das Knotenobjekt eingefügt, aus dem die Sammlung erstellt wurde.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie verwenden.[`ImportNode`](../../documentbase/importnode/) um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

## Beispiele

Zeigt, wie ein neuer Abschnittsknoten für die Bearbeitung vorbereitet wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument besteht aus einem Abschnitt, der einen Hauptteil hat, der wiederum einen Absatz enthält.
// Wir können diesem Dokument Inhalte hinzufügen, indem wir diesem Absatz Elemente wie Textläufe, Formen oder Tabellen hinzufügen.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Wenn wir einen neuen Abschnitt wie diesen hinzufügen, hat er weder einen Hauptteil noch andere untergeordnete Knoten.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Führen Sie die Methode „EnsureMinimum“ aus, um diesem Abschnitt einen Hauptteil und einen Absatz hinzuzufügen und mit der Bearbeitung zu beginnen.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [Node](../../node/)
* class [NodeCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
