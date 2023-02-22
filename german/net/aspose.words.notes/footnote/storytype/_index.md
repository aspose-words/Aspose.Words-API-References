---
title: Footnote.StoryType
second_title: Aspose.Words für .NET-API-Referenz
description: Footnote eigendom. gibt zurück StoryType.Fußnoten oder StoryType.Endnotes .
type: docs
weight: 60
url: /de/net/aspose.words.notes/footnote/storytype/
---
## Footnote.StoryType property

gibt zurück **StoryType.Fußnoten** oder **StoryType.Endnotes** .

```csharp
public override StoryType StoryType { get; }
```

### Beispiele

Zeigt, wie InlineStory-Knoten eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tabellenknoten haben eine "EnsureMinimum()"-Methode, die sicherstellt, dass die Tabelle mindestens eine Zelle hat.
Table table = new Table(doc);
table.EnsureMinimum();

// Wir können eine Tabelle in eine Fußnote einfügen, wodurch sie in der Fußzeile der verweisenden Seite erscheint.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Eine InlineStory hat auch eine "EnsureMinimum()"-Methode, aber in diesem Fall
// es stellt sicher, dass das letzte untergeordnete Element des Knotens ein Absatz ist,
// damit wir Text in Microsoft Word einfach anklicken und schreiben können.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Bearbeiten Sie das Erscheinungsbild des Ankers, der die kleine hochgestellte Zahl ist
// im Haupttext, der auf die Fußnote zeigt.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Alle Inline-Story-Knoten haben ihre jeweiligen Story-Typen.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Ein Kommentar ist eine andere Art von Inline-Story.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Der übergeordnete Absatz eines Inline-Story-Knotens ist derjenige aus dem Haupttext des Dokuments.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Der letzte Absatz ist jedoch derjenige aus dem Inhalt des Kommentartextes,
// die sich außerhalb des Hauptdokumentkörpers in einer Sprechblase befindet.
// Ein Kommentar hat standardmäßig keine untergeordneten Knoten,
// so können wir auch hier die Methode CertainMinimum() anwenden, um einen Absatz zu platzieren.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Sobald wir einen Absatz haben, können wir den Builder dazu bewegen und unseren Kommentar schreiben.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Siehe auch

* enum [StoryType](../../../aspose.words/storytype/)
* class [Footnote](../)
* namensraum [Aspose.Words.Notes](../../footnote/)
* Montage [Aspose.Words](../../../)


