---
title: FileFormatUtil.ExtensionToSaveFormat
second_title: Aspose.Words per .NET API Reference
description: FileFormatUtil metodo. Converte lestensione del nome file in un fileSaveFormat valore.
type: docs
weight: 40
url: /it/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Converte l'estensione del nome file in un file[`SaveFormat`](../../saveformat/) valore.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| extension | String | L'estensione del file. Può essere con o senza punto iniziale. Senza distinzione tra maiuscole e minuscole. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentNullException | Genera se il parametro è`nullo`. |

### Osservazioni

Se l'estensione non può essere riconosciuta, ritornaUnknown.

### Esempi

Mostra come utilizzare i metodi FileFormatUtil per rilevare il formato di un documento.

```csharp
// Carica un documento da un file a cui manca un'estensione di file, quindi rileva il formato del file.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Di seguito sono riportati due metodi per convertire un LoadFormat nel corrispondente SaveFormat.
    // 1 - Ottieni la stringa dell'estensione del file per LoadFormat, quindi ottieni il corrispondente SaveFormat da quella stringa:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Converti LoadFormat direttamente nel suo SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Carica un documento dallo stream, quindi salvalo nell'estensione di file rilevata automaticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Guarda anche

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* spazio dei nomi [Aspose.Words](../../fileformatutil/)
* assemblea [Aspose.Words](../../../)


