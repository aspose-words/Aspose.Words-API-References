---
title: SaveOptions.UpdateFields
second_title: Aspose.Words per .NET API Reference
description: SaveOptions proprietà. Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà èVERO .
type: docs
weight: 160
url: /it/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` .

```csharp
public bool UpdateFields { get; set; }
```

### Osservazioni

Permette di specificare se imitare o meno il comportamento di MS Word.

### Esempi

Mostra come aggiornare tutti i campi di un documento immediatamente prima di salvarlo in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci testo con i campi PAGE e NUMPAGES. Questi campi non visualizzano il valore corretto in tempo reale.
// Dovremo aggiornarli manualmente utilizzando metodi di aggiornamento come "Field.Update()" e "Document.UpdateFields()"
// ogni volta che ne abbiamo bisogno per visualizzare valori accurati.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "UpdateFields" su "false" per non aggiornare tutti i campi in un documento subito prima di un'operazione di salvataggio.
// Questa è l'opzione preferibile se sappiamo che tutti i nostri campi saranno aggiornati prima del salvataggio.
// Imposta la proprietà "UpdateFields" su "true" per scorrere tutto il documento
// campi e aggiornarli prima di salvarlo come PDF. Ciò assicurerà che tutti i campi vengano visualizzati
// i valori più accurati nel PDF.
options.UpdateFields = updateFields;

// Possiamo clonare oggetti PdfSaveOptions.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../saveoptions/)
* assemblea [Aspose.Words](../../../)


