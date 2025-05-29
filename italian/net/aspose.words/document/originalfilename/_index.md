---
title: Document.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words per .NET
description: Recupera facilmente il nome file originale del tuo documento con la proprietà Document OriginalFileName. Migliora il tuo flusso di lavoro e la tua organizzazione oggi stesso!
type: docs
weight: 300
url: /it/net/aspose.words/document/originalfilename/
---
## Document.OriginalFileName property

Ottiene il nome del file originale del documento.

```csharp
public string OriginalFileName { get; }
```

## Osservazioni

Resi`null` se il documento è stato caricato da un flusso o creato vuoto.

## Esempi

Mostra come recuperare i dettagli dell'operazione di caricamento di un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

Mostra come utilizzare i metodi FileFormatUtil per rilevare il formato di un documento.

```csharp
// Carica un documento da un file a cui manca un'estensione, quindi rileva il formato del file.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel suo SaveFormat corrispondente.
    // 1 - Ottieni la stringa dell'estensione del file per LoadFormat, quindi ottieni il SaveFormat corrispondente da quella stringa:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Converti LoadFormat direttamente nel suo SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dal flusso e salvalo nell'estensione di file rilevata automaticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
