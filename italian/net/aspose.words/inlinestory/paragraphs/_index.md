---
title: InlineStory.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words per .NET
description: Scopri la proprietà Paragrafi InlineStory e accedi a una raccolta unica di paragrafi di storie per una migliore organizzazione e leggibilità dei contenuti.
type: docs
weight: 80
url: /it/net/aspose.words/inlinestory/paragraphs/
---
## InlineStory.Paragraphs property

Ottiene una raccolta di paragrafi che sono figli immediati della storia.

```csharp
public ParagraphCollection Paragraphs { get; }
```

## Esempi

Mostra come aggiungere un commento a un paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // In Microsoft Word, possiamo fare clic con il pulsante destro del mouse su questo commento nel corpo del documento per modificarlo o per rispondere.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Mostra come inserire e personalizzare le note a piè di pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungi del testo e fai riferimento ad esso con una nota a piè di pagina. Questa nota inserirà un piccolo riferimento in apice.
// contrassegna dopo il testo a cui fa riferimento e crea una voce sotto il testo principale in fondo alla pagina.
// Questa voce conterrà il segno di riferimento della nota a piè di pagina e il testo di riferimento,
// che passeremo al metodo "InsertFootnote" del generatore di documenti.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Se questa proprietà è impostata su "true", il segno di riferimento della nostra nota a piè di pagina
// sarà il suo indice tra tutte le note a piè di pagina della sezione.
// Questa è la prima nota a piè di pagina, quindi il segno di riferimento sarà "1".
Assert.True(footnote.IsAuto);

 // Possiamo spostare il generatore di documenti all'interno della nota a piè di pagina per modificarne il testo di riferimento.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Possiamo impostare un segno di riferimento personalizzato che la nota a piè di pagina utilizzerà al posto del suo numero di indice.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Un segnalibro con il flag "IsAuto" impostato su true mostrerà comunque il suo indice reale
// anche se i segnalibri precedenti visualizzano riferimenti personalizzati, il riferimento di questo segnalibro sarà "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Guarda anche

* class [ParagraphCollection](../../paragraphcollection/)
* class [InlineStory](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
