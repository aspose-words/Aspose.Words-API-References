---
title: Section.EnsureMinimum
second_title: Aspose.Words für .NET-API-Referenz
description: Section methode. Stellt sicher dass der Abschnitt einen Hauptteil mit einem Absatz hat.
type: docs
weight: 130
url: /de/net/aspose.words/section/ensureminimum/
---
## Section.EnsureMinimum method

Stellt sicher, dass der Abschnitt einen Hauptteil mit einem Absatz hat.

```csharp
public void EnsureMinimum()
```

### Beispiele

Zeigt, wie Sie einen neuen Abschnittsknoten für die Bearbeitung vorbereiten.

```csharp
Document doc = new Document();

// Ein leeres Dokument hat einen Abschnitt, der einen Körper hat, der wiederum einen Absatz hat.
// Wir können diesem Dokument Inhalte hinzufügen, indem wir diesem Absatz Elemente wie Textläufe, Formen oder Tabellen hinzufügen.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Wenn wir einen neuen Abschnitt wie diesen hinzufügen, hat er keinen Hauptteil oder andere untergeordnete Knoten.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Führen Sie die "EnsureMinimum"-Methode aus, um diesem Abschnitt einen Hauptteil und einen Absatz hinzuzufügen, um mit der Bearbeitung zu beginnen.
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


