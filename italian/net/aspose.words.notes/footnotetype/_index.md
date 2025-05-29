---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.FootnoteType. Distingui facilmente tra note a piè di pagina e note di chiusura per una formattazione e una chiarezza migliori dei documenti.
type: docs
weight: 5020
url: /it/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Specifica se si tratta di una nota a piè di pagina o di una nota di chiusura.

```csharp
public enum FootnoteType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Footnote | `0` | L'oggetto è una nota a piè di pagina. |
| Endnote | `1` | L'oggetto è una nota di chiusura. |

## Osservazioni

Sia le note a piè di pagina che le note di chiusura sono rappresentate da oggetti tramite l'Footnote Classe . Usa[`FootnoteType`](../footnote/footnotetype/) per distinguere tra note a piè di pagina e note di chiusura.

## Esempi

Mostra come fare riferimento al testo con una nota a piè di pagina e una nota di chiusura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// quindi il marcatore visualizzato nel corpo del testo verrà numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Inserisci altro testo e contrassegnalo con una nota di chiusura con un segno di riferimento personalizzato,
// che verrà utilizzato al posto del numero "2" e impostare "IsAuto" su false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al testo a cui si fa riferimento,
// quindi questa interruzione di pagina non influirà sulla nota a piè di pagina.
// D'altra parte, le note di chiusura sono sempre alla fine del documento
// in modo che questa interruzione di pagina sposti la nota di chiusura alla pagina successiva.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
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

* spazio dei nomi [Aspose.Words.Notes](../../aspose.words.notes/)
* assemblea [Aspose.Words](../../)
