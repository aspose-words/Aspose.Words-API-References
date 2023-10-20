---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words per .NET
description: Footnote FootnoteType proprietà. Restituisce un valore che specifica se si tratta di una nota a piè di pagina o di chiusura in C#.
type: docs
weight: 20
url: /it/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Restituisce un valore che specifica se si tratta di una nota a piè di pagina o di chiusura.

```csharp
public FootnoteType FootnoteType { get; }
```

## Esempi

Mostra la differenza tra note a piè di pagina e note di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per allegare riferimenti numerati al testo. Entrambi questi riferimenti aggiungeranno a
// piccolo segno di riferimento in apice nella posizione in cui li inseriamo.
// Il segno di riferimento, per impostazione predefinita, è il numero di indice del riferimento tra tutti i riferimenti nel documento.
// Ogni riferimento creerà anche una voce, che avrà lo stesso segno di riferimento del corpo del testo
// e testo di riferimento, che passeremo al metodo "InsertFootnote" del generatore di documenti.
// 1 - Una nota a piè di pagina, la cui voce apparirà sulla stessa pagina del testo a cui fa riferimento:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - Una nota finale, la cui voce apparirà alla fine del documento:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### Guarda anche

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
