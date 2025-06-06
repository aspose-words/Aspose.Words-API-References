---
title: FieldRef Class
linktitle: FieldRef
articleTitle: FieldRef
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldRef per un'implementazione fluida dei campi REF. Migliora l'automazione dei documenti e semplifica il tuo flusso di lavoro oggi stesso!
type: docs
weight: 2740
url: /it/net/aspose.words.fields/fieldref/
---
## FieldRef class

Implementa il campo REF.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldRef : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldRef](fieldref/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | Ottiene o imposta il nome del segnalibro a cui si fa riferimento. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | Ottiene o imposta se incrementare i numeri delle note a piè di pagina, delle note di chiusura e delle annotazioni contrassegnate dal segnalibro e inserire il testo corrispondente delle note a piè di pagina, delle note di chiusura e dei commenti. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | Ottiene o imposta se creare un collegamento ipertestuale al paragrafo aggiunto ai segnalibri. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | Ottiene o imposta se inserire il numero del paragrafo a cui si fa riferimento esattamente come appare nel documento. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | Ottiene o imposta se inserire il numero del paragrafo a cui si fa riferimento nel contesto completo. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | Ottiene o imposta se inserire il numero del paragrafo a cui si fa riferimento nel contesto relativo. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | Ottiene o imposta se inserire la posizione relativa del paragrafo a cui si fa riferimento. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | Ottiene o imposta se sopprimere i caratteri non delimitatori. |
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

Inserisce il testo o la grafica rappresentati dal segnalibro specificato.

## Esempi

Mostra come creare testo con segnalibro con un campo SET e poi visualizzarlo nel documento utilizzando un campo REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Assegna un nome al testo aggiunto ai preferiti con un campo SET.
// Questo campo si riferisce al "segnalibro", non a una struttura di segnalibro che appare all'interno del testo, ma a una variabile denominata.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Fare riferimento al segnalibro tramite il nome in un campo REF e visualizzarne il contenuto.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Mostra come inserire campi REF per fare riferimento ai segnalibri.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Applicheremo un formato di elenco personalizzato, in cui la quantità di parentesi angolari indica il livello di elenco in cui ci troviamo attualmente.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Inserire un campo REF che conterrà il testo all'interno del nostro segnalibro, fungerà da collegamento ipertestuale e clonerà le note a piè di pagina del segnalibro.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Inserisce un campo RIF. e visualizza se il segnalibro a cui si fa riferimento si trova sopra o sotto di esso.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Visualizza il numero dell'elenco del segnalibro così come appare nel documento.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Visualizza il numero dell'elenco dei segnalibri, omettendo però i caratteri non delimitatori, come le parentesi angolari.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Spostarsi di un livello nell'elenco.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Visualizza il numero dell'elenco del segnalibro e i numeri di tutti i livelli di elenco superiori.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Visualizza i numeri del livello di elenco tra questo campo REF e il segnalibro a cui fa riferimento.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Alla fine del documento, il segnalibro verrà visualizzato come elemento dell'elenco.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// Fai in modo che il generatore di documenti inserisca un campo REF, faccia riferimento a un segnalibro con esso e aggiunga del testo prima e dopo.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
