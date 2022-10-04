---
title: FieldIndex
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo INDEX.
type: docs
weight: 1910
url: /it/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

Implementa il campo INDEX.

```csharp
public class FieldIndex : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldIndex](fieldindex/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare l'indice. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare i riferimenti incrociati e altre voci. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Ottiene o imposta un tipo di voce di indice utilizzato per creare l'indice. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Ottiene un valore che indica se un separatore del numero di pagina viene sovrascritto tramite il codice del campo. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Ottiene un valore che indica se una sequenza deve essere utilizzata durante la creazione del risultato del campo. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Ottiene o imposta un'intestazione che appare all'inizio di ogni serie di voci per una determinata lettera. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Ottiene o imposta l'ID lingua utilizzato per generare l'indice. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Ottiene o imposta un intervallo di lettere a cui limitare l'indice. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Ottiene o imposta il numero di colonne per pagina utilizzate durante la creazione dell'indice. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare due numeri di pagina in un elenco di numeri di pagina. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare una voce di indice e il relativo numero di pagina. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare l'inizio e la fine di un intervallo di pagine. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Ottiene o imposta se eseguire voci secondarie nella stessa riga della voce principale. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Ottiene o imposta il nome di una sequenza il cui numero è incluso nel numero di pagina. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Ottiene o imposta se abilitare l'uso del testo yomi per le voci dell'indice. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Crea un indice utilizzando le voci di indice specificate dai campi XE e inserisce quell'indice in questo punto del documento.

### Esempi

Mostra come creare un campo INDEX e quindi utilizzare i campi XE per popolarlo con le voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro
// e la pagina contenente il campo XE a destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDEX li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configura il campo INDEX solo per visualizzare i campi XE che rientrano nei limiti
// di un segnalibro denominato "MainBookmark" e le cui proprietà "EntryType" hanno valore "A".
// Per entrambi i campi INDEX e XE, la proprietà "EntryType" utilizza solo il primo carattere del relativo valore stringa.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// In una nuova pagina, avvia il segnalibro con un nome che corrisponda al valore
// della proprietà "NomeSegnalibro" del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Il campo INDEX raccoglierà questa voce perché è all'interno del segnalibro,
// e il suo tipo di voce corrisponde anche al tipo di voce del campo INDEX.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Inserisci un campo XE che non comparirà nell'INDICE perché i tipi di voce non corrispondono.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Termina il segnalibro e inserisci un campo XE in seguito.
// È dello stesso tipo del campo INDEX, ma non apparirà
// poiché è al di fuori dei limiti del segnalibro.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Mostra come popolare un campo INDEX con voci utilizzando i campi XE e come modificarne l'aspetto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDEX che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE a destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDEX li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// L'impostazione del valore di questa proprietà su "A" raggrupperà tutte le voci in base alla prima lettera,
// e metti quella lettera in maiuscolo sopra ogni gruppo.
index.Heading = "A";

// Imposta la tabella creata dal campo INDEX in modo che si estenda su 2 colonne.
index.NumberOfColumns = "2";

// Imposta tutte le voci con lettere iniziali al di fuori dell'intervallo di caratteri "ac" da omettere.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// I prossimi due campi XE verranno visualizzati sotto l'intestazione "A",
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

// Entrambi i prossimi due campi XE saranno sotto un'intestazione "B" e "C" nel sommario dei campi INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// I campi INDEX ordinano tutte le voci in ordine alfabetico, quindi questa voce verrà visualizzata sotto "A" con le altre due.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Questa voce non apparirà perché inizia con la lettera "D",
// che non rientra nell'intervallo di caratteri "ac" definito dalla proprietà LetterRange del campo INDEX.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
