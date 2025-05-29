---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: Aspose.Words per .NET
description: Trasforma facilmente i valori del formato di caricamento in estensioni di file con il metodo LoadFormatToExtension di FileFormatUtil. Ottieni estensioni minuscole precise con facilità!
type: docs
weight: 60
url: /it/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Converte un valore enumerato del formato di caricamento in un'estensione di file. L'estensione restituita è una stringa minuscola con un punto iniziale.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Genera un errore quando non è possibile convertire. |

## Osservazioni

ILWordML il valore viene convertito in ".wml".

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
