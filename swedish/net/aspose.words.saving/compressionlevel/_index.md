---
title: Enum CompressionLevel
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.CompressionLevel uppräkning. Komprimeringsnivå för OOXMLfiler.
type: docs
weight: 4610
url: /sv/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Komprimeringsnivå för OOXML-filer.

(DOCX- och DOTX-filer är internt ett ZIP-arkiv, den här egenskapen styr komprimeringsnivån för arkivet.

Observera att FlatOpc-filen inte är ett ZIP-arkiv, därför påverkar den här egenskapen inte FlatOpc-filerna.)

```csharp
public enum CompressionLevel
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | `0` | Normal komprimeringsnivå. Standard komprimeringsnivå som används av Aspose.Words. |
| Maximum | `1` | Maximal komprimeringsnivå. |
| Fast | `2` | Snabb komprimeringsnivå. |
| SuperFast | `3` | Supersnabb komprimeringsnivå. Microsoft Word använder denna komprimeringsnivå. |

### Exempel

Visar hur man anger vilken komprimeringsnivå som ska användas när ett OOXML-dokument sparas.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions-objekt
// och skicka det sedan till dokumentets sparmetod för att ändra hur vi sparar dokumentet.
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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


