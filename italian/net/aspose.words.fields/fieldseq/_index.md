---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldSeq per un'implementazione fluida dei campi SEQ. Migliora l'automazione dei tuoi documenti con potenti funzionalità e flessibilità.
type: docs
weight: 2800
url: /it/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

Implementa il campo SEQ.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldSeq : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldSeq](fieldseq/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Ottiene o imposta un nome di segnalibro che fa riferimento a un elemento in un'altra posizione del documento anziché nella posizione corrente. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Ottiene o imposta se inserire il numero di sequenza successivo per l'elemento specificato. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Ottiene o imposta un numero intero che rappresenta un livello di intestazione a cui reimpostare il numero di sequenza. Restituisce -1 se il numero è assente. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Ottiene o imposta un numero intero a cui reimpostare il numero di sequenza. Restituisce -1 se il numero è assente. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Ottiene o imposta il nome assegnato alla serie di elementi da numerare. |
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

Numera in sequenza capitoli, tabelle, figure e altri elenchi di elementi definiti dall'utente in un documento.

## Esempi

Mostra come creare una numerazione utilizzando i campi SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che visualizzerà il valore del conteggio corrente di "MySequence",
// dopo aver utilizzato la proprietà "ResetNumber" per impostarla su 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Visualizza il numero successivo in questa sequenza con un altro campo SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Inserire un'intestazione di livello 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Inserire un altro campo SEQ dalla stessa sequenza e configurarlo per reimpostare il conteggio a ogni intestazione con 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// L'intestazione sopra è un'intestazione di livello 1, quindi il conteggio per questa sequenza viene reimpostato a 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Passa al numero successivo di questa sequenza.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Mostra come combinare i campi indice e sequenza.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che contiene il campo SEQ,
// e il numero della pagina in cui appare il campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configurare questo campo TOC in modo che abbia una proprietà SequenceIdentifier con il valore "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Configura questo campo TOC per selezionare solo i campi SEQ che rientrano nei limiti di un segnalibro
// denominato "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserire un campo SEQ che abbia un identificatore di sequenza che corrisponda al TOC
// Proprietà TableOfFiguresLabel. Questo campo non creerà una voce nel sommario poiché è esterno
// i limiti del segnalibro designati da "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è compresa nei limiti del segnalibro.
// Il paragrafo che contiene questo campo verrà visualizzato nell'indice come voce.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La sequenza di questo campo SEQ non corrisponde alla proprietà "TableOfFiguresLabel" del TOC,
// e rientra nei limiti del segnalibro. Il relativo paragrafo non verrà visualizzato nell'indice come voce.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è compresa nei limiti del segnalibro.
// Questo campo fa riferimento anche a un altro segnalibro. Il contenuto di quel segnalibro apparirà nella voce dell'indice di questo campo SEQ.
// Il campo SEQ stesso non visualizzerà il contenuto di quel segnalibro.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Crea un segnalibro con contenuti che verranno visualizzati nella voce TOC grazie al campo SEQ soprastante che vi fa riferimento.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

Mostra come popolare un campo TOC con voci utilizzando i campi SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che include il campo SEQ e il numero di pagina in cui appare il campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Utilizzare la proprietà "TableOfFiguresLabel" per assegnare un nome alla sequenza principale per l'indice.
// Ora, questo TOC creerà voci solo dai campi SEQ con il loro "SequenceIdentifier" impostato su "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Possiamo nominare un'altra sequenza di campi SEQ nella proprietà "PrefixedSequenceIdentifier".
 // I campi SEQ di questa sequenza di prefissi non creeranno voci TOC.
// Ogni voce TOC creata da un campo SEQ della sequenza principale ora visualizzerà anche il conteggio che
// la sequenza del prefisso è attualmente attiva nel campo SEQ della sequenza primaria che ha creato la voce.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Ogni voce del TOC visualizzerà il conteggio della sequenza del prefisso immediatamente a sinistra
// del numero di pagina in cui appare il campo SEQ della sequenza principale.
// Possiamo specificare un separatore personalizzato che apparirà tra questi due numeri.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Esistono due modi per utilizzare i campi SEQ per popolare questo indice.
// 1 - Inserimento di un campo SEQ appartenente alla sequenza di prefissi del TOC:
// Questo campo incrementerà di 1 il conteggio delle sequenze SEQ per "PrefixSequence".
// Poiché questo campo non appartiene alla sequenza principale identificata
// tramite la proprietà "TableOfFiguresLabel" del TOC, non verrà visualizzato come voce.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Inserimento di un campo SEQ appartenente alla sequenza principale del TOC:
// Questo campo SEQ creerà una voce nel sommario.
// La voce TOC conterrà il paragrafo in cui si trova il campo SEQ e il numero della pagina in cui appare.
// Questa voce mostrerà anche il conteggio attuale della sequenza di prefissi,
// separato dal numero di pagina dal valore della proprietà SeqenceSeparator del TOC.
// Il conteggio "PrefixSequence" è a 1, questo campo SEQ della sequenza principale si trova a pagina 2,
// e il separatore è ">", quindi la voce visualizzerà "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Inserisce una pagina, fa avanzare di 2 la sequenza del prefisso e inserisce un campo SEQ per creare in seguito una voce di sommario.
// La sequenza del prefisso è ora a 2 e il campo SEQ della sequenza principale è a pagina 3,
// quindi la voce TOC visualizzerà "2>3" al suo conteggio di pagine.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
