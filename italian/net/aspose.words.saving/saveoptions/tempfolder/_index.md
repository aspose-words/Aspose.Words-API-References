---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words per .NET
description: Ottimizza il salvataggio dei documenti con la proprietà SaveOptions TempFolder, che designa una cartella per i file DOC e DOCX temporanei, migliorando l'efficienza.
type: docs
weight: 140
url: /it/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei.

```csharp
public string TempFolder { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| OutOfMemoryException | Da generare se si sta salvando un documento molto grande (migliaia di pagine) e/o si stanno elaborando molti documenti contemporaneamente. Il picco di memoria durante il salvataggio può essere abbastanza significativo da causare l'eccezione. |

## Osservazioni

Quando Aspose.Words salva un documento, deve creare strutture interne temporanee. Per impostazione predefinita, queste strutture interne vengono create in memoria e l'utilizzo della memoria subisce un picco per un breve periodo durante il salvataggio del documento. Al termine del salvataggio, la memoria viene liberata e recuperata dal garbage collector.

Specificare una cartella temporanea utilizzando`TempFolder` Farà sì che Aspose.Words mantenga le strutture interne nei file temporanei invece che nella memoria. Riduce l'utilizzo di memoria durante il salvataggio, ma ne ridurrà le prestazioni.

La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Al termine del salvataggio, Aspose.Words elimina automaticamente tutti i file temporanei.

## Esempi

Mostra come utilizzare il disco rigido anziché la memoria quando si salva un documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando salviamo un documento, vari elementi vengono temporaneamente memorizzati nella memoria mentre è in corso l'operazione di salvataggio.
// Possiamo usare questa opzione per usare una cartella temporanea nel file system locale,
// che ridurrà il sovraccarico di memoria della nostra applicazione.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// La cartella temporanea specificata deve esistere nel file system locale prima dell'operazione di salvataggio.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// La cartella persisterà senza alcun contenuto residuo dall'operazione di caricamento.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
