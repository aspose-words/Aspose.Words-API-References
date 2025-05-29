---
title: FieldIndex.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldIndex EntryType per gestire in modo efficiente i tipi di voci di indice per un'indicizzazione ottimizzata e prestazioni di ricerca migliorate.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

Ottiene o imposta un tipo di voce di indice utilizzato per creare l'indice.

```csharp
public string EntryType { get; set; }
```

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

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
