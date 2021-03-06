---
title: ForcePageBreaks
second_title: Aspose.Words per .NET API Reference
description: Consente di specificare se le interruzioni di pagina devono essere conservate durante lesportazione.
type: docs
weight: 30
url: /it/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Consente di specificare se le interruzioni di pagina devono essere conservate durante l'esportazione.

Il valore predefinito è **falso**.

```csharp
public bool ForcePageBreaks { get; set; }
```

### Osservazioni

La proprietà ha effetto solo sulle interruzioni di pagina inserite in modo esplicito in un documento. Non è correlato alle interruzioni di pagina che MS Word inserisce automaticamente alla fine di ogni pagina.

### Esempi

Mostra come specificare se conservare le interruzioni di pagina durante l'esportazione di un documento in testo normale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al "Salva" del documento
// metodo per modificare il modo in cui salviamo il documento come testo normale.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Gli oggetti "Documento" di Aspose.Words hanno interruzioni di pagina, proprio come i documenti di Microsoft Word.
// I formati di salvataggio come ".txt" sono un corpo di testo continuo senza interruzioni di pagina.
// Imposta la proprietà "ForcePageBreaks" su "true" per preservare tutte le interruzioni di pagina sotto forma di caratteri '\f'.
// Imposta la proprietà "ForcePageBreaks" su "false" per eliminare tutte le interruzioni di pagina.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Se carichiamo un documento in chiaro con interruzioni di pagina,
// l'oggetto "Documento" li utilizzerà per dividere il corpo in pagine.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Guarda anche

* class [TxtSaveOptionsBase](../../txtsaveoptionsbase)
* spazio dei nomi [Aspose.Words.Saving](../../txtsaveoptionsbase)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
