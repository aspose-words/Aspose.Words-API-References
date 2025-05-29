---
title: InlineStory.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words für .NET
description: Entdecken Sie InlineStory-Tabellen. Greifen Sie auf eine Sammlung von Story-Tabellen zu, die Ihre Datenorganisation und Ihr Storytelling verbessern. Jetzt entdecken!
type: docs
weight: 110
url: /de/net/aspose.words/inlinestory/tables/
---
## InlineStory.Tables property

Ruft eine Sammlung von Tabellen ab, die unmittelbare untergeordnete Elemente der Story sind.

```csharp
public TableCollection Tables { get; }
```

## Beispiele

Zeigt, wie InlineStory-Knoten eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tabellenknoten haben eine Methode „EnsureMinimum()“, die sicherstellt, dass die Tabelle mindestens eine Zelle hat.
Table table = new Table(doc);
table.EnsureMinimum();

// Wir können eine Tabelle in eine Fußnote einfügen, sodass sie in der Fußzeile der Referenzseite angezeigt wird.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Eine InlineStory hat auch eine "EnsureMinimum()"-Methode, aber in diesem Fall
// es stellt sicher, dass das letzte untergeordnete Element des Knotens ein Absatz ist,
// damit wir in Microsoft Word einfach klicken und Text schreiben können.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Bearbeiten Sie das Erscheinungsbild des Ankers, der die kleine hochgestellte Zahl ist
// im Haupttext, der auf die Fußnote verweist.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Alle Inline-Story-Knoten haben ihre jeweiligen Story-Typen.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Ein Kommentar ist eine andere Art von Inline-Story.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Der übergeordnete Absatz eines Inline-Story-Knotens ist der aus dem Haupttext des Dokuments.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Der letzte Absatz ist jedoch der aus dem Kommentartextinhalt,
// das sich außerhalb des Hauptdokumenttexts in einer Sprechblase befindet.
// Ein Kommentar hat standardmäßig keine untergeordneten Knoten,
// daher können wir die Methode EnsureMinimum() anwenden, um auch hier einen Absatz einzufügen.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Sobald wir einen Absatz haben, können wir den Builder dazu bewegen, ihn zu erstellen und unseren Kommentar zu schreiben.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Siehe auch

* class [TableCollection](../../../aspose.words.tables/tablecollection/)
* class [InlineStory](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
