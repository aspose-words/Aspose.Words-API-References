---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: Discover the OoxmlSaveOptions CompressionLevel property to optimize document saving with customizable compression levels for enhanced performance.
type: docs
weight: 30
url: /net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Specifies the compression level used to save document. The default value is Normal.

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Examples

Shows how to specify the compression level to use while saving an OOXML document.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// When we save the document to an OOXML format, we can create an OoxmlSaveOptions object
// and then pass it to the document's saving method to modify how we save the document.
// Set the "CompressionLevel" property to "CompressionLevel.Maximum" to apply the strongest and slowest compression.
// Set the "CompressionLevel" property to "CompressionLevel.Normal" to apply
// the default compression that Aspose.Words uses while saving OOXML documents.
// Set the "CompressionLevel" property to "CompressionLevel.Fast" to apply a faster and weaker compression.
// Set the "CompressionLevel" property to "CompressionLevel.SuperFast" to apply
// the default compression that Microsoft Word uses.
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

### See Also

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
