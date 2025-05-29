---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words per .NET
description: Migliora le prestazioni dei documenti con la proprietà MemoryOptimization di SaveOptions. Controlla l'utilizzo della memoria prima del salvataggio, aumentando efficienza e velocità.
type: docs
weight: 100
url: /it/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Osservazioni

Impostando questa opzione su`VERO` può ridurre significativamente il consumo di memoria salvando documenti di grandi dimensioni a scapito di tempi di salvataggio più lenti.

## Esempi

Mostra un'opzione per ottimizzare il consumo di memoria durante il rendering di documenti di grandi dimensioni in PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Impostare la proprietà "MemoryOptimization" su "true" per ridurre l'occupazione di memoria delle operazioni di salvataggio di documenti di grandi dimensioni
// a costo di aumentare la durata dell'operazione.
// Impostare la proprietà "MemoryOptimization" su "false" per salvare normalmente il documento come PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
