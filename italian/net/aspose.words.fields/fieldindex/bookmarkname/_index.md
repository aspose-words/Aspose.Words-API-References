---
title: FieldIndex.BookmarkName
second_title: Aspose.Words per .NET API Reference
description: FieldIndex proprietà. Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare lindice.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldindex/bookmarkname/
---
## FieldIndex.BookmarkName property

Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare l'indice.

```csharp
public string BookmarkName { get; set; }
```

### Esempi

Mostra come creare un campo INDICE e quindi utilizzare i campi XE per compilarlo con le voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro
// e la pagina contenente il campo XE sulla destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDICE li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Configura il campo INDEX solo per visualizzare i campi XE che rientrano nei limiti
// di un segnalibro denominato "MainBookmark" e le cui proprietà "EntryType" hanno un valore "A".
// Per entrambi i campi INDEX e XE, la proprietà "EntryType" utilizza solo il primo carattere del suo valore di stringa.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// In una nuova pagina, inizia il segnalibro con un nome che corrisponde al valore
// della proprietà "BookmarkName" del campo INDICE.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Il campo INDICE rileverà questa voce perché è all'interno del segnalibro,
// e il suo tipo di voce corrisponde anche al tipo di voce del campo INDICE.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Inserisci un campo XE che non apparirà nell'INDICE perché i tipi di voce non corrispondono.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Termina il segnalibro e successivamente inserisce un campo XE.
// È dello stesso tipo del campo INDEX, ma non verrà visualizzato
// poiché è fuori dai confini del segnalibro.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldindex/)
* assemblea [Aspose.Words](../../../)


