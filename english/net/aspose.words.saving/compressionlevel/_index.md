---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Saving.CompressionLevel enum to optimize OOXML file sizes, enhancing performance and efficiency in document processing.
type: docs
weight: 5610
url: /net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Compression level for OOXML files.

(DOCX and DOTX files are internally a ZIP-archive, this property controls the compression level of the archive.

Note, that FlatOpc file is not a ZIP-archive, therefore, this property does not affect the FlatOpc files.)

```csharp
public enum CompressionLevel
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | `0` | Normal compression level. Default compression level used by Aspose.Words. |
| Maximum | `1` | Maximum compression level. |
| Fast | `2` | Fast compression level. |
| SuperFast | `3` | Super Fast compression level. Microsoft Word uses this compression level. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
