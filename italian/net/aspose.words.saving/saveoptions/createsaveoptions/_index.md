---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words per .NET
description: Scopri il metodo CreateSaveOptions per generare facilmente opzioni di salvataggio personalizzate per il tuo formato preferito, migliorando l'efficienza della gestione dei documenti.
type: docs
weight: 10
url: /it/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

Crea un oggetto di opzioni di salvataggio di una classe adatta al formato di salvataggio specificato.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | SaveFormat | Formato di salvataggio per il quale creare un oggetto opzioni di salvataggio. |

### Valore di ritorno

Un oggetto di una classe che deriva da[`SaveOptions`](../).

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

Crea un oggetto di opzioni di salvataggio di una classe adatta all'estensione di file specificata nel nome file specificato.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | L'estensione di questo nome file determina la classe dell'oggetto opzioni di salvataggio da creare. |

### Valore di ritorno

Un oggetto di una classe che deriva da[`SaveOptions`](../).

## Esempi

Mostra come impostare un modello predefinito per i documenti che non hanno modelli allegati.

```csharp
Document doc = new Document();

// Abilita l'aggiornamento automatico dello stile, ma non allegare un documento modello.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Poiché non esiste un documento modello, il documento non aveva alcun posto in cui tenere traccia delle modifiche di stile.
// Utilizzare un oggetto SaveOptions per impostare automaticamente un modello
// se un documento che stiamo salvando non ne ha uno.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
