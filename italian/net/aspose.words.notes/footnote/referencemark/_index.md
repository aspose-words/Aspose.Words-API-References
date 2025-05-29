---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words per .NET
description: Personalizza le tue note a piè di pagina con la proprietà ReferenceMark. Imposta facilmente marcatori univoci per garantire chiarezza e organizzazione nei tuoi documenti. Migliora la leggibilità oggi stesso!
type: docs
weight: 60
url: /it/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Ottiene/imposta il segno di riferimento personalizzato da utilizzare per questa nota a piè di pagina. Il valore predefinito è **stringa vuota** (Empty ), il che significa che vengono utilizzate note a piè di pagina numerate automaticamente.

```csharp
public string ReferenceMark { get; set; }
```

## Osservazioni

Se questa proprietà è impostata su**stringa vuota** (Empty ) O`null` , Poi[`IsAuto`](../isauto/) la proprietà verrà impostata automaticamente su`VERO` , se impostato su qualsiasi altra cosa allora[`IsAuto`](../isauto/) sarà impostato su`falso` .

Il formato RTF può memorizzare solo 1 simbolo come segno di riferimento personalizzato, quindi durante l'esportazione verrà scritto solo il primo simbolo, gli altri verranno scartati.

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

* class [Footnote](../)
* spazio dei nomi [Aspose.Words.Notes](../../../aspose.words.notes/)
* assemblea [Aspose.Words](../../../)
