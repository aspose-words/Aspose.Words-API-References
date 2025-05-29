---
title: FileFormatUtil.LoadFormatToSaveFormat
linktitle: LoadFormatToSaveFormat
articleTitle: LoadFormatToSaveFormat
second_title: Aspose.Words per .NET
description: Converti facilmente LoadFormat in SaveFormat con il metodo LoadFormatToSaveFormat di FileFormatUtil. Semplifica la gestione dei tuoi file oggi stesso!
type: docs
weight: 70
url: /it/net/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil.LoadFormatToSaveFormat method

Converte un[`LoadFormat`](../../loadformat/) valore a un[`SaveFormat`](../../saveformat/) valore se possibile.

```csharp
public static SaveFormat LoadFormatToSaveFormat(LoadFormat loadFormat)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Genera un errore quando non è possibile convertire. |

## Esempi

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

* enum [SaveFormat](../../saveformat/)
* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
