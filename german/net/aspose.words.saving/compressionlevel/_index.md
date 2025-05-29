---
title: CompressionLevel Enum
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.CompressionLevel, um die Größe von OOXML-Dateien zu optimieren und so die Leistung und Effizienz bei der Dokumentverarbeitung zu verbessern.
type: docs
weight: 5610
url: /de/net/aspose.words.saving/compressionlevel/
---
## CompressionLevel enumeration

Komprimierungsstufe für OOXML-Dateien.

(DOCX- und DOTX-Dateien sind intern ein ZIP-Archiv, diese Eigenschaft steuert den Komprimierungsgrad des Archivs.

Beachten Sie, dass die FlatOpc-Datei kein ZIP-Archiv ist. Daher wirkt sich diese Eigenschaft nicht auf die FlatOpc-Dateien aus.)

```csharp
public enum CompressionLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | `0` | Normale Komprimierungsstufe. Standardmäßige Komprimierungsstufe, die von Aspose.Words verwendet wird. |
| Maximum | `1` | Maximale Komprimierungsstufe. |
| Fast | `2` | Schnelle Komprimierungsstufe. |
| SuperFast | `3` | Superschnelle Komprimierungsstufe. Microsoft Word verwendet diese Komprimierungsstufe. |

## Beispiele

Zeigt, wie Sie die zu verwendende Komprimierungsstufe beim Speichern eines OOXML-Dokuments angeben.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.Maximum“, um die stärkste und langsamste Komprimierung anzuwenden.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.Normal“, um sie anzuwenden
// die Standardkomprimierung, die Aspose.Words beim Speichern von OOXML-Dokumenten verwendet.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.Fast“, um eine schnellere und schwächere Komprimierung anzuwenden.
// Setzen Sie die Eigenschaft „CompressionLevel“ auf „CompressionLevel.SuperFast“, um sie anzuwenden
// die von Microsoft Word verwendete Standardkomprimierung.
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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
