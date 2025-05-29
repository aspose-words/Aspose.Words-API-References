---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words für .NET
description: Greifen Sie mit der Eigenschaft „Story LastParagraph“ mühelos auf den letzten Absatz Ihrer Story zu und verbessern Sie so Ihr Erlebnis bei der Verwaltung und Bearbeitung von Erzählungen.
type: docs
weight: 20
url: /de/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Ruft den letzten Absatz der Geschichte ab.

```csharp
public Paragraph LastParagraph { get; }
```

## Beispiele

Zeigt, wie die Cursorposition eines DocumentBuilder zu einem angegebenen Knoten verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Der Dokument-Builder verfügt über einen Cursor, der als Teil des Dokuments fungiert
// wo der Builder neue Knoten anfügt, wenn wir seine Methoden zur Dokumenterstellung verwenden.
// Dieser Cursor funktioniert auf die gleiche Weise wie der blinkende Cursor von Microsoft Word.
// und es endet auch immer unmittelbar nach einem Knoten, den der Builder gerade eingefügt hat.
// Um Inhalt an einen anderen Teil des Dokuments anzuhängen,
// Wir können den Cursor mit der Methode „MoveTo“ zu einem anderen Knoten verschieben.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Der Cursor steht jetzt vor dem Knoten, zu dem wir ihn verschoben haben.
// Wenn Sie einen zweiten Lauf hinzufügen, wird dieser vor dem ersten Lauf eingefügt.
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
