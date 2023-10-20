---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words per .NET
description: SaveOptions TempFolder proprietà. Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà ènullo e non vengono utilizzati file temporanei in C#.
type: docs
weight: 140
url: /it/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei.

```csharp
public string TempFolder { get; set; }
```

## Osservazioni

Quando Aspose.Words salva un documento, è necessario creare strutture interne temporanee. Per impostazione predefinita, queste strutture interne vengono create in memoria e l'utilizzo della memoria aumenta per un breve periodo mentre il documento viene salvato. Al termine del salvataggio, la memoria viene liberata e recuperata dal Garbage Collector.

Se stai salvando un documento molto grande (migliaia di pagine) e/o elaborando molti documenti contemporaneamente, , il picco di memoria durante il salvataggio può essere abbastanza significativo da causare un blocco del sistemaOutOfMemoryException . Specificare una cartella temporanea utilizzando`TempFolder` farà sì che Aspose.Words mantenga le strutture interne nei file temporanei anziché nella memoria. Riduce l'utilizzo della memoria durante il salvataggio, ma diminuirà le prestazioni di salvataggio.

La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Aspose.Words elimina automaticamente tutti i file temporanei al termine del salvataggio.

## Esempi

Mostra come utilizzare il disco rigido anziché la memoria durante il salvataggio di un documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando salviamo un documento, vari elementi vengono temporaneamente archiviati in memoria mentre è in corso l'operazione di salvataggio.
// Possiamo usare questa opzione per usare invece una cartella temporanea nel file system locale,
// che ridurrà il sovraccarico di memoria della nostra applicazione.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// La cartella temporanea specificata deve esistere nel file system locale prima dell'operazione di salvataggio.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// La cartella persisterà senza contenuti residui dall'operazione di caricamento.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
