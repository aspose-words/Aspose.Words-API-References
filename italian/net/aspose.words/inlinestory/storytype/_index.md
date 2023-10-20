---
title: InlineStory.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words per .NET
description: InlineStory StoryType proprietà. Restituisce il tipo della storia in C#.
type: docs
weight: 100
url: /it/net/aspose.words/inlinestory/storytype/
---
## InlineStory.StoryType property

Restituisce il tipo della storia.

```csharp
public abstract StoryType StoryType { get; }
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

// Possiamo inserire una tabella all'interno di una nota a piè di pagina, che la farà apparire nel piè di pagina della pagina di riferimento.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Anche una InlineStory ha un metodo "EnsureMinimum()", ma in questo caso
// si assicura che l'ultimo figlio del nodo sia un paragrafo,
// per poter fare clic e scrivere facilmente testo in Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Modifica l'aspetto dell'ancora, che è il piccolo numero in apice
// nel testo principale che punta alla nota a piè di pagina.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Tutti i nodi della storia in linea hanno i rispettivi tipi di storia.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Un commento è un altro tipo di storia in linea.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Il paragrafo principale di un nodo della storia in linea sarà quello del corpo del documento principale.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Tuttavia, l'ultimo paragrafo è quello del contenuto del testo del commento,
// che sarà all'esterno del corpo principale del documento in un fumetto.
// Un commento non avrà nodi figli per impostazione predefinita,
// così possiamo applicare il metodo GuaranteeMinimum() per inserire un paragrafo anche qui.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Una volta che abbiamo un paragrafo, possiamo spostare il builder per farlo e scrivere il nostro commento.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Guarda anche

* enum [StoryType](../../storytype/)
* class [InlineStory](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
