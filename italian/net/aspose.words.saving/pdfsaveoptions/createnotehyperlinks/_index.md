---
title: PdfSaveOptions.CreateNoteHyperlinks
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Specifica se convertire i riferimenti alle note a piè di pagina/note di chiusura nel brano del testo principale in collegamenti ipertestuali attivi. Quando si fa clic il collegamento ipertestuale porterà alla nota a piè di pagina/nota di chiusura corrispondente. Limpostazione predefinita èfalso .
type: docs
weight: 50
url: /it/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Specifica se convertire i riferimenti alle note a piè di pagina/note di chiusura nel brano del testo principale in collegamenti ipertestuali attivi. Quando si fa clic, il collegamento ipertestuale porterà alla nota a piè di pagina/nota di chiusura corrispondente. L'impostazione predefinita è`falso` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

### Esempi

Mostra come fare in modo che le note a piè di pagina e le note di chiusura funzionino come collegamenti ipertestuali.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "CreateNoteHyperlinks" su "true" per trasformare tutti i simboli delle note a piè di pagina/note di chiusura
// nel testo fungono da link che, cliccando, ci portano alle rispettive note a piè di pagina/note di chiusura.
// Imposta la proprietà "CreateNoteHyperlinks" su "false" per evitare che i simboli delle note a piè di pagina/note finali si colleghino a qualcosa.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


