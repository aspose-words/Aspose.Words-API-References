---
title: FieldNoteRef Class
linktitle: FieldNoteRef
articleTitle: FieldNoteRef
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldNoteRef per un'integrazione perfetta dei campi NOTEREF, migliorando il riferimento e la gestione dei documenti.
type: docs
weight: 2610
url: /it/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

Implementa il campo NOTEREF.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldNoteRef : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldNoteRef](fieldnoteref/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname/) { get; set; } | Ottiene o imposta il nome del segnalibro. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | Ottiene o imposta se inserire un collegamento ipertestuale al paragrafo aggiunto ai segnalibri. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | Inserisce il segno di riferimento con la stessa formattazione del carattere dello stile Riferimento nota a piè di pagina o Riferimento nota di chiusura. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | Ottiene o imposta se inserire una posizione relativa del paragrafo con segnalibro. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Inserisce il segno della nota a piè di pagina o della nota di chiusura contrassegnata dal segnalibro specificato.

## Esempi

Mostra come creare riferimenti incrociati alle note a piè di pagina con il campo NOTEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("CrossReference: ");

FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, false); // <--- non aggiornare il campo
field.BookmarkName = "CrossRefBookmark";
field.InsertHyperlink = true;
field.InsertReferenceMark = true;
field.InsertRelativePosition = false;
builder.Writeln();

builder.StartBookmark("CrossRefBookmark");
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Cross referenced footnote.");
builder.EndBookmark("CrossRefBookmark");
builder.Writeln();

doc.UpdateFields();

// Questo campo funziona solo nelle versioni precedenti di Microsoft Word.
doc.Save(ArtifactsDir + "Field.NOTEREF.doc");
```

Mostra come inserire campi NOTEREF e modificarne l'aspetto.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un segnalibro con una nota a piè di pagina a cui farà riferimento il campo NOTEREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Questo campo NOTEREF visualizzerà il numero della nota a piè di pagina all'interno del segnalibro a cui si fa riferimento.
    // Impostando la proprietà InsertHyperlink possiamo passare al segnalibro premendo Ctrl + clic sul campo in Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Quando si utilizza il flag \p, dopo il numero della nota a piè di pagina, il campo visualizza anche la posizione del segnalibro rispetto al campo stesso.
    // Bookmark1 si trova sopra questo campo e contiene la nota a piè di pagina numero 1, quindi il risultato sarà "1 sopra" in caso di aggiornamento.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 si trova sotto questo campo e contiene la nota a piè di pagina numero 2, quindi il campo visualizzerà "2 sotto".
    // Il flag \f fa sì che il numero 2 venga visualizzato nello stesso formato dell'etichetta del numero della nota a piè di pagina nel testo effettivo.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un campo NOTEREF con le proprietà specificate.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un segnalibro denominato con una nota a piè di pagina alla fine.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
