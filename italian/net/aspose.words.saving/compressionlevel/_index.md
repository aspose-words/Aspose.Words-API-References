---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.CompressionLevel per ottimizzare le dimensioni dei file OOXML, migliorando le prestazioni e l'efficienza nell'elaborazione dei documenti.
type: docs
weight: 5610
url: /it/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Livello di compressione per i file OOXML.

(I file DOCX e DOTX sono internamente un archivio ZIP, questa proprietà controlla il livello di compressione dell'archivio.

Nota che il file FlatOpc non è un archivio ZIP, pertanto questa proprietà non influisce sui file FlatOpc.)

```csharp
public enum CompressionLevel
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | `0` | Livello di compressione normale. Livello di compressione predefinito utilizzato da Aspose.Words. |
| Maximum | `1` | Livello di compressione massimo. |
| Fast | `2` | Livello di compressione veloce. |
| SuperFast | `3` | Livello di compressione Super Veloce. Microsoft Word utilizza questo livello di compressione. |

## Esempi

Mostra come specificare il livello di compressione da utilizzare durante il salvataggio di un documento OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e quindi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Impostare la proprietà "CompressionLevel" su "CompressionLevel.Maximum" per applicare la compressione più forte e più lenta.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Normal" per applicare
// la compressione predefinita utilizzata da Aspose.Words durante il salvataggio dei documenti OOXML.
// Impostare la proprietà "CompressionLevel" su "CompressionLevel.Fast" per applicare una compressione più rapida e più debole.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.SuperFast" per applicare
// la compressione predefinita utilizzata da Microsoft Word.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
