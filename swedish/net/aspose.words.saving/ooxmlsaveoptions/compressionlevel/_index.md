---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words för .NET
description: Upptäck egenskapen OoxmlSaveOptions CompressionLevel för att optimera dokumentsparandet med anpassningsbara komprimeringsnivåer för förbättrad prestanda.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Anger komprimeringsnivån som används för att spara dokumentet. Standardvärdet ärNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Exempel

Visar hur man anger komprimeringsnivån som ska användas när man sparar ett OOXML-dokument.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions-objekt
// och skicka den sedan till dokumentets sparmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.Maximum" för att tillämpa den starkaste och långsammaste komprimeringen.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.Normal" för att tillämpa
// standardkomprimeringen som Aspose.Words använder när OOXML-dokument sparas.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.Fast" för att tillämpa en snabbare och svagare komprimering.
// Ställ in egenskapen "CompressionLevel" till "CompressionLevel.SuperFast" för att tillämpa
// standardkomprimeringen som Microsoft Word använder.
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

### Se även

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
