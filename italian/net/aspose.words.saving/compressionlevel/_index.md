---
title: Enum CompressionLevel
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.CompressionLevel enum. Livello di compressione per file OOXML.
type: docs
weight: 4870
url: /it/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Livello di compressione per file OOXML.

(i file DOCX e DOTX sono internamente un archivio ZIP, questa proprietà controlla il livello di compressione dell'archivio.

Tieni presente che il file FlatOpc non è un archivio ZIP, pertanto questa proprietà non influisce sui file FlatOpc.)

```csharp
public enum CompressionLevel
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Normal | `0` | Livello di compressione normale. Livello di compressione predefinito utilizzato da Aspose.Words. |
| Maximum | `1` | Livello massimo di compressione. |
| Fast | `2` | Livello di compressione veloce. |
| SuperFast | `3` | Livello di compressione super veloce. Microsoft Word utilizza questo livello di compressione. |

### Esempi

Mostra come specificare il livello di compressione da utilizzare durante il salvataggio di un documento OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e poi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Maximum" per applicare la compressione più forte e più lenta.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Normal" da applicare
// la compressione predefinita utilizzata da Aspose.Words durante il salvataggio dei documenti OOXML.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.Fast" per applicare una compressione più veloce e più debole.
// Imposta la proprietà "CompressionLevel" su "CompressionLevel.SuperFast" da applicare
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


