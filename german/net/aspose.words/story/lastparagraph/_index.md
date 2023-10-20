---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words für .NET
description: Story LastParagraph eigendom. Ruft den letzten Absatz in der Geschichte ab in C#.
type: docs
weight: 20
url: /de/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Ruft den letzten Absatz in der Geschichte ab.

```csharp
public Paragraph LastParagraph { get; }
```

## Beispiele

Zeigt, wie die Cursorposition eines DocumentBuilders auf einen angegebenen Knoten verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Der Document Builder verfügt über einen Cursor, der als Teil des Dokuments fungiert
// wo der Builder neue Knoten anhängt, wenn wir seine Dokumenterstellungsmethoden verwenden.
// Dieser Cursor funktioniert auf die gleiche Weise wie der blinkende Cursor von Microsoft Word.
// und es endet auch immer unmittelbar nach jedem Knoten, den der Builder gerade eingefügt hat.
// Um Inhalt an einen anderen Teil des Dokuments anzuhängen,
// Mit der Methode „MoveTo“ können wir den Cursor auf einen anderen Knoten bewegen.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Der Cursor befindet sich jetzt vor dem Knoten, auf den wir ihn verschoben haben.
// Durch Hinzufügen eines zweiten Laufs wird dieser vor dem ersten Lauf eingefügt.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Bewegen Sie den Cursor an das Ende des Dokuments, um wie zuvor mit dem Anhängen von Text am Ende fortzufahren.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
