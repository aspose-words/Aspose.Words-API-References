---
title: InlineStory.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words per .NET
description: Scopri la proprietà ParentParagraph di InlineStory per accedere senza sforzo al paragrafo padre di qualsiasi nodo, migliorando la tua esperienza di gestione dei contenuti.
type: docs
weight: 90
url: /it/net/aspose.words/inlinestory/parentparagraph/
---
## InlineStory.ParentParagraph property

Recupera il genitore[`Paragraph`](../../paragraph/) di questo nodo.

```csharp
public Paragraph ParentParagraph { get; }
```

## Esempi

Mostra come inserire i nodi InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// I nodi della tabella hanno un metodo "EnsureMinimum()" che assicura che la tabella abbia almeno una cella.
Table table = new Table(doc);
table.EnsureMinimum();

// Possiamo inserire una tabella all'interno di una nota a piè di pagina, in modo che venga visualizzata nel piè di pagina della pagina di riferimento.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Anche un InlineStory ha un metodo "EnsureMinimum()", ma in questo caso,
// si assicura che l'ultimo figlio del nodo sia un paragrafo,
// per consentirci di cliccare e scrivere facilmente il testo in Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Modifica l'aspetto dell'ancora, che è il piccolo numero in apice
// nel testo principale che rimanda alla nota a piè di pagina.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Tutti i nodi della storia in linea hanno i rispettivi tipi di storia.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Un commento è un altro tipo di storia in linea.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Il paragrafo padre di un nodo di una storia in linea sarà quello del corpo del documento principale.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Tuttavia, l'ultimo paragrafo è quello del contenuto del testo del commento,
// che sarà visualizzato all'esterno del corpo del documento principale, in un fumetto.
// Per impostazione predefinita, un commento non avrà alcun nodo figlio,
// quindi possiamo applicare il metodo EnsureMinimum() per inserire un paragrafo anche qui.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Una volta creato il paragrafo, possiamo far partire il builder per scriverlo e scrivere il nostro commento.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Guarda anche

* class [Paragraph](../../paragraph/)
* class [InlineStory](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
