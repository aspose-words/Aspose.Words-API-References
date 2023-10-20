---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words per .NET
description: LoadOptions TempFolder proprietà. Permette di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà ènullo e non vengono utilizzati file temporanei in C#.
type: docs
weight: 150
url: /it/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Permette di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei.

```csharp
public string TempFolder { get; set; }
```

## Osservazioni

La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Aspose.Words elimina automaticamente tutti i file temporanei al termine della lettura.

## Esempi

Mostra come caricare un documento utilizzando file temporanei.

```csharp
// Tieni presente che un approccio di questo tipo può ridurre l'utilizzo della memoria ma riduce la velocità
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Assicurarsi che la directory esista e venga caricata
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Mostra come utilizzare il disco rigido anziché la memoria durante il caricamento di un documento.

```csharp
// Quando carichiamo un documento, vari elementi vengono temporaneamente archiviati in memoria mentre avviene l'operazione di salvataggio.
// Possiamo usare questa opzione per usare invece una cartella temporanea nel file system locale,
// che ridurrà il sovraccarico di memoria della nostra applicazione.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// La cartella temporanea specificata deve esistere nel file system locale prima dell'operazione di caricamento.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// La cartella persisterà senza contenuti residui dall'operazione di caricamento.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
