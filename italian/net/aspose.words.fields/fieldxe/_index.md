---
title: FieldXE Class
linktitle: FieldXE
articleTitle: FieldXE
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldXE, la soluzione ideale per implementare in modo efficiente i campi XE nell'elaborazione dei documenti. Migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 3020
url: /it/net/aspose.words.fields/fieldxe/
---
## FieldXE class

Implementa il campo XE.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldXE : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldXE](fieldxe/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [EntryType](../../aspose.words.fields/fieldxe/entrytype/) { get; set; } | Ottiene o imposta un tipo di voce di indice. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsBold](../../aspose.words.fields/fieldxe/isbold/) { get; set; } | Ottiene o imposta se applicare la formattazione in grassetto al numero di pagina della voce. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsItalic](../../aspose.words.fields/fieldxe/isitalic/) { get; set; } | Ottiene o imposta se applicare la formattazione corsiva al numero di pagina della voce. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PageNumberReplacement](../../aspose.words.fields/fieldxe/pagenumberreplacement/) { get; set; } | Ottiene o imposta il testo utilizzato al posto di un numero di pagina. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldxe/pagerangebookmarkname/) { get; set; } | Ottiene o imposta il nome del segnalibro che contrassegna un intervallo di pagine inserito come numero di pagina della voce. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [Text](../../aspose.words.fields/fieldxe/text/) { get; set; } | Ottiene o imposta il testo della voce. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [Yomi](../../aspose.words.fields/fieldxe/yomi/) { get; set; } | Ottiene o imposta lo yomi (primo carattere fonetico per l'ordinamento degli indici) per la voce di indice |

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

Definisce il testo e il numero di pagina per una voce di indice, utilizzata da un campo INDICE.

## Esempi

Mostra come creare un campo INDICE e quindi utilizzare i campi XE per popolarlo con voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro
// e la pagina contenente il campo XE sulla destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDICE li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configurare il campo INDICE solo per visualizzare i campi XE che rientrano nei limiti
// di un segnalibro denominato "MainBookmark" e le cui proprietà "EntryType" hanno il valore "A".
// Sia per i campi INDEX che XE, la proprietà "EntryType" utilizza solo il primo carattere del suo valore stringa.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// In una nuova pagina, avvia il segnalibro con un nome che corrisponda al valore
// della proprietà "BookmarkName" del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Il campo INDICE rileverà questa voce perché si trova all'interno del segnalibro,
// e il suo tipo di voce corrisponde anche al tipo di voce del campo INDICE.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Inserire un campo XE che non verrà visualizzato nell'INDICE perché i tipi di voce non corrispondono.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Termina il segnalibro e inserisci un campo XE in seguito.
// È dello stesso tipo del campo INDICE, ma non verrà visualizzato
// poiché si trova al di fuori dei limiti del segnalibro.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Mostra come popolare un campo INDICE con voci utilizzando campi XE e come modificarne l'aspetto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDICE li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Impostando il valore di questa proprietà su "A" tutte le voci verranno raggruppate in base alla loro prima lettera,
// e posiziona quella lettera in maiuscolo sopra ogni gruppo.
index.Heading = "A";

// Imposta la tabella creata dal campo INDEX in modo che si estenda su 2 colonne.
index.NumberOfColumns = "2";

// Imposta l'omissione di tutte le voci con lettere iniziali al di fuori dell'intervallo di caratteri "ac".
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Questi due campi XE successivi verranno visualizzati sotto l'intestazione "A",
// con i rispettivi stili di testo applicati anche ai numeri di pagina.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// I due campi XE successivi saranno sotto le intestazioni "B" e "C" nella tabella dei contenuti dei campi INDICE.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// I campi INDEX ordinano tutte le voci in ordine alfabetico, quindi questa voce verrà visualizzata sotto "A" insieme alle altre due.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Questa voce non verrà visualizzata perché inizia con la lettera "D",
// che è al di fuori dell'intervallo di caratteri "ac" definito dalla proprietà LetterRange del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
