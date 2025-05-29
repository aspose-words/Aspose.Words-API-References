---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words per .NET
description: Scopri la proprietà CompressionLevel di OoxmlSaveOptions per ottimizzare il salvataggio dei documenti con livelli di compressione personalizzabili per prestazioni migliorate.
type: docs
weight: 30
url: /it/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Specifica il livello di compressione utilizzato per salvare il documento. Il valore predefinito èNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

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

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
