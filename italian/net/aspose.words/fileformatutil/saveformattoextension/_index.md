---
title: FileFormatUtil.SaveFormatToExtension
linktitle: SaveFormatToExtension
articleTitle: SaveFormatToExtension
second_title: Aspose.Words per .NET
description: Converti facilmente i valori del formato di salvataggio in estensioni di file con il metodo SaveFormatToExtension di FileFormatUtil. Ottieni estensioni minuscole precise con facilità!
type: docs
weight: 80
url: /it/net/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil.SaveFormatToExtension method

Converte un valore enumerato del formato di salvataggio in un'estensione di file. L'estensione restituita è una stringa minuscola con un punto iniziale.

```csharp
public static string SaveFormatToExtension(SaveFormat saveFormat)
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentException | Genera un errore quando non è possibile convertire. |

## Osservazioni

ILWordML il valore viene convertito in ".wml".

ILFlatOpc il valore viene convertito in ".fopc".

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
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
