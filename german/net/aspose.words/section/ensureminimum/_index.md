---
title: Section.EnsureMinimum
second_title: Aspose.Words für .NET-API-Referenz
description: Section methode. Stellt sicher dass der Abschnitt vorhanden istBody mit einerParagraph .
type: docs
weight: 150
url: /de/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Stellt sicher, dass der Abschnitt vorhanden ist[`Body`](../body/) mit einer[`Paragraph`](../../paragraph/) .

```csharp
public void EnsureMinimum()
```

### Beispiele

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

* class [Section](../)
* namensraum [Aspose.Words](../../section/)
* Montage [Aspose.Words](../../../)


