---
title: Footnote.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words für .NET
description: Footnote StoryType eigendom. Gibt zurückFootnotes oderEndnotes  in C#.
type: docs
weight: 60
url: /de/net/aspose.words.notes/footnote/storytype/
---
## Footnote.StoryType property

Gibt zurückFootnotes oderEndnotes .

```csharp
public override StoryType StoryType { get; }
```

## Beispiele

Zeigt, wie InlineStory-Knoten eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tabellenknoten verfügen über eine „EnsureMinimum()“-Methode, die sicherstellt, dass die Tabelle mindestens eine Zelle enthält.
Table table = new Table(doc);
table.EnsureMinimum();

// Wir können eine Tabelle in eine Fußnote einfügen, wodurch sie in der Fußzeile der verweisenden Seite erscheint.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Eine InlineStory hat auch eine „EnsureMinimum()“-Methode, aber in diesem Fall
// es stellt sicher, dass das letzte untergeordnete Element des Knotens ein Absatz ist,
// Damit wir problemlos in Microsoft Word klicken und Texte schreiben können.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Bearbeiten Sie das Erscheinungsbild des Ankers, bei dem es sich um die kleine hochgestellte Zahl handelt
// im Haupttext, der auf die Fußnote verweist.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Alle Inline-Story-Knoten haben ihre jeweiligen Story-Typen.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Ein Kommentar ist eine andere Art von Inline-Story.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Der übergeordnete Absatz eines Inline-Story-Knotens ist derjenige aus dem Hauptdokumentkörper.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Allerdings ist der letzte Absatz derjenige aus dem Kommentartextinhalt,
// der sich außerhalb des Hauptdokumentkörpers in einer Sprechblase befindet.
// Ein Kommentar hat standardmäßig keine untergeordneten Knoten.
// damit wir auch hier die Methode ConsiderMinimum() anwenden können, um einen Absatz zu platzieren.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Sobald wir einen Absatz haben, können wir den Builder dazu veranlassen, ihn auszuführen und unseren Kommentar zu schreiben.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Siehe auch

* enum [StoryType](../../../aspose.words/storytype/)
* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../../aspose.words.notes/)
* Montage [Aspose.Words](../../../)
