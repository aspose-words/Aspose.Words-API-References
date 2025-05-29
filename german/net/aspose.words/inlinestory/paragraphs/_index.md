---
title: InlineStory.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „InlineStory-Absätze“ und greifen Sie auf eine einzigartige Sammlung von Story-Absätzen zu, um die Inhaltsorganisation und Lesbarkeit zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words/inlinestory/paragraphs/
---
## InlineStory.Paragraphs property

Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Story sind.

```csharp
public ParagraphCollection Paragraphs { get; }
```

## Beispiele

Zeigt, wie man einem Absatz einen Kommentar hinzufügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

    // In Microsoft Word können wir mit der rechten Maustaste auf diesen Kommentar im Dokumenttext klicken, um ihn zu bearbeiten oder darauf zu antworten.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Zeigt, wie Fußnoten eingefügt und angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und mit einer Fußnote darauf verweisen. Diese Fußnote enthält einen kleinen hochgestellten Verweis
// Markieren Sie nach dem Text, auf den verwiesen wird, und erstellen Sie einen Eintrag unter dem Haupttext am unteren Seitenrand.
// Dieser Eintrag enthält das Referenzzeichen und den Referenztext der Fußnote,
// die wir an die Methode „InsertFootnote“ des Dokument-Generators übergeben.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wenn diese Eigenschaft auf "true" gesetzt ist, dann ist das Referenzzeichen unserer Fußnote
// wird sein Index unter allen Fußnoten des Abschnitts sein.
// Dies ist die erste Fußnote, daher lautet das Referenzzeichen „1“.
Assert.True(footnote.IsAuto);

    // Wir können den Dokumentgenerator in die Fußnote verschieben, um den Referenztext zu bearbeiten.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wir können ein benutzerdefiniertes Referenzzeichen festlegen, das die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ein Lesezeichen mit dem Flag "IsAuto" auf true wird immer noch seinen tatsächlichen Index anzeigen
// Auch wenn vorherige Lesezeichen benutzerdefinierte Referenzzeichen anzeigen, ist das Referenzzeichen dieses Lesezeichens eine „3“.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Siehe auch

* class [ParagraphCollection](../../paragraphcollection/)
* class [InlineStory](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
