---
title: OoxmlSaveOptions.CompressionLevel
second_title: Aspose.Words für .NET-API-Referenz
description: OoxmlSaveOptions eigendom. Gibt die Komprimierungsstufe an die zum Speichern des Dokuments verwendet wird. Der Standardwert istNormal .
type: docs
weight: 30
url: /de/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Gibt die Komprimierungsstufe an, die zum Speichern des Dokuments verwendet wird. Der Standardwert istNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

### Beispiele

Zeigt, wie Sie die Komprimierungsstufe angeben, die beim Speichern eines OOXML-Dokuments verwendet werden soll.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.Maximum“, um die stärkste und langsamste Komprimierung anzuwenden.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.Normal“, um sie anzuwenden
// die Standardkomprimierung, die Aspose.Words beim Speichern von OOXML-Dokumenten verwendet.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.Fast“, um eine schnellere und schwächere Komprimierung anzuwenden.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.SuperFast“, um sie anzuwenden
// die Standardkomprimierung, die Microsoft Word verwendet.
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

### Siehe auch

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* Montage [Aspose.Words](../../../)


