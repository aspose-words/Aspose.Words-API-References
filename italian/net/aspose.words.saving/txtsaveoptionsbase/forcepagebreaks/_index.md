---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words per .NET
description: Controlla le interruzioni di pagina con la proprietà ForcePageBreaks di TxtSaveOptionsBase. Garantisci esportazioni fluide e mantieni la formattazione dei documenti senza sforzo.
type: docs
weight: 30
url: /it/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Consente di specificare se le interruzioni di pagina devono essere mantenute durante l'esportazione.

Il valore predefinito è`falso`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Osservazioni

La proprietà riguarda solo le interruzioni di pagina inserite esplicitamente in un documento. Non è correlata alle interruzioni di pagina che MS Word inserisce automaticamente alla fine di ogni pagina.

## Esempi

Mostra come specificare se mantenere le interruzioni di pagina quando si esporta un documento in testo normale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al "Save" del documento
// metodo per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Gli oggetti "Documento" di Aspose.Words hanno interruzioni di pagina, proprio come i documenti di Microsoft Word.
// I formati di salvataggio come ".txt" sono un unico corpo di testo continuo, senza interruzioni di pagina.
// Impostare la proprietà "ForcePageBreaks" su "true" per conservare tutte le interruzioni di pagina nella forma di caratteri '\f'.
// Impostare la proprietà "ForcePageBreaks" su "false" per ignorare tutte le interruzioni di pagina.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Se carichiamo un documento di testo normale con interruzioni di pagina,
// l'oggetto "Documento" li utilizzerà per dividere il corpo in pagine.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Guarda anche

* class [TxtSaveOptionsBase](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
