---
title: Section.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihren Inhalt mit der EnsureMinimum-Methode und stellen Sie sicher, dass jeder Abschnitt einen Hauptteil mit einem Absatz enthält, um die Klarheit und Struktur zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Stellt sicher, dass der Abschnitt[`Body`](../body/) mit einem[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

## Beispiele

Zeigt, wie ein neuer Abschnittsknoten für die Bearbeitung vorbereitet wird.

```csharp
Document doc = new Document();

// Ein leeres Dokument besteht aus einem Abschnitt mit einem Hauptteil, der wiederum einen Absatz enthält.
// Wir können diesem Dokument Inhalte hinzufügen, indem wir diesem Absatz Elemente wie Textläufe, Formen oder Tabellen hinzufügen.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Wenn wir einen neuen Abschnitt wie diesen hinzufügen, hat er weder einen Hauptteil noch andere untergeordnete Knoten.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Führen Sie die Methode „EnsureMinimum“ aus, um diesem Abschnitt einen Textkörper und einen Absatz hinzuzufügen und mit der Bearbeitung zu beginnen.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
