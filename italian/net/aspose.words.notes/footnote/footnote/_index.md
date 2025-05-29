---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words per .NET
description: Crea note a piè di pagina accattivanti senza sforzo con il nostro Footnote Constructor. Migliora la chiarezza e la professionalità dei tuoi contenuti in pochi clic!
type: docs
weight: 10
url: /it/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Inizializza un'istanza di[`Footnote`](../) classe.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | DocumentBase | Il documento del proprietario. |
| footnoteType | FootnoteType | UN[`FootnoteType`](../footnotetype/) value che specifica se si tratta di una nota a piè di pagina o di una nota di chiusura. |

## Osservazioni

Quando[`Footnote`](../) viene creato, appartiene al documento specificato, ma non è ancora parte del documento e[`ParentNode`](../../../aspose.words/node/parentnode/) È`null`.

Per aggiungere[`Footnote`](../) all'uso del documento[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) O[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) sul paragrafo in cui vuoi inserire la nota a piè di pagina.

## Esempi

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
