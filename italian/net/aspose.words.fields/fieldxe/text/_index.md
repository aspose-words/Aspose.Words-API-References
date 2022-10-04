---
title: Text
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta il testo della voce.
type: docs
weight: 70
url: /it/net/aspose.words.fields/fieldxe/text/
---
## FieldXE.Text property

Ottiene o imposta il testo della voce.

```csharp
public string Text { get; set; }
```

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

* class [FieldXE](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldxe/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
