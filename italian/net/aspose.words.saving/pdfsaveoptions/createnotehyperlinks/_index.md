---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words per .NET
description: Migliora i tuoi PDF con CreateNoteHyperlinks di PdfSaveOptions. Converti note a piè di pagina e note di chiusura in link cliccabili per una facile navigazione. Impostazione predefinita false.
type: docs
weight: 60
url: /it/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Specifica se convertire i riferimenti alle note a piè di pagina/note di chiusura nel testo principale del racconto in collegamenti ipertestuali attivi. Quando si fa clic, il collegamento ipertestuale porterà alla nota a piè di pagina/nota di chiusura corrispondente. L'impostazione predefinita è`falso` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Esempi

Mostra come far funzionare le note a piè di pagina e le note di chiusura come collegamenti ipertestuali.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "CreateNoteHyperlinks" su "true" per trasformare tutti i simboli delle note a piè di pagina/note di chiusura
// nel testo fungono da link che, cliccando, ci portano alle rispettive note a piè di pagina/note di chiusura.
// Impostare la proprietà "CreateNoteHyperlinks" su "false" per evitare che i simboli delle note a piè di pagina/note di chiusura siano collegati a nulla.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
